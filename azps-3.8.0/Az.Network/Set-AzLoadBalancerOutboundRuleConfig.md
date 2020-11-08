---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 82e61d3c4a387630dec2c829d651f8d9746a3419
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090231"
---
# <span data-ttu-id="c57e0-101">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c57e0-101">Set-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="c57e0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c57e0-102">SYNOPSIS</span></span>
<span data-ttu-id="c57e0-103">Ställer in en konfiguration för utgående regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="c57e0-103">Sets an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="c57e0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c57e0-104">SYNTAX</span></span>

### <span data-ttu-id="c57e0-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="c57e0-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c57e0-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c57e0-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c57e0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c57e0-107">DESCRIPTION</span></span>
<span data-ttu-id="c57e0-108">Cmdleten **set-AzLoadBalancerOutboundRuleConfig** ställer in en konfiguration för utgående regel för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="c57e0-108">The **Set-AzLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="c57e0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c57e0-109">EXAMPLES</span></span>

### <span data-ttu-id="c57e0-110">Exempel 1: ändra konfigurationen för utgående regel på en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="c57e0-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="c57e0-111">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i $slb variabel.</span><span class="sxs-lookup"><span data-stu-id="c57e0-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="c57e0-112">Det andra kommandot använder pipeline-operatorn för att överföra belastningsutjämnaren i $slb till Add-AzLoadBalancerOutboundRuleConfig, som lägger till en regel för utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="c57e0-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="c57e0-113">Det tredje kommandot skickar belastningsutjämnaren till **set-AzLoadBalancerOutboundRuleConfig** , som sparar och uppdaterar konfigurationen för utgående regel.</span><span class="sxs-lookup"><span data-stu-id="c57e0-113">The third command passes the load balancer to **Set-AzLoadBalancerOutboundRuleConfig** , which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="c57e0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c57e0-114">PARAMETERS</span></span>

### <span data-ttu-id="c57e0-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="c57e0-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="c57e0-116">Antalet utgående portar som ska användas för NAT.</span><span class="sxs-lookup"><span data-stu-id="c57e0-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="c57e0-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c57e0-117">-BackendAddressPool</span></span>
<span data-ttu-id="c57e0-118">En referens till en pool med DIP.</span><span class="sxs-lookup"><span data-stu-id="c57e0-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="c57e0-119">Utgående trafik bal anse ras slumpmässigt för IP i Server delen.</span><span class="sxs-lookup"><span data-stu-id="c57e0-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="c57e0-120">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c57e0-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="c57e0-121">En referens till en pool med DIP.</span><span class="sxs-lookup"><span data-stu-id="c57e0-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="c57e0-122">Utgående trafik bal anse ras slumpmässigt för IP i Server delen.</span><span class="sxs-lookup"><span data-stu-id="c57e0-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="c57e0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c57e0-123">-DefaultProfile</span></span>
<span data-ttu-id="c57e0-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c57e0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c57e0-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c57e0-125">-EnableTcpReset</span></span>
<span data-ttu-id="c57e0-126">Ta emot dubbelriktad TCP-återställning i TCP-flödets tids gräns för inaktivitet eller oväntat upphör Ande.</span><span class="sxs-lookup"><span data-stu-id="c57e0-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="c57e0-127">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="c57e0-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c57e0-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c57e0-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c57e0-129">Belastnings utjämningens IP-adresser för klient delen.</span><span class="sxs-lookup"><span data-stu-id="c57e0-129">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="c57e0-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c57e0-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c57e0-131">Timeout för TCP-inaktiv anslutning</span><span class="sxs-lookup"><span data-stu-id="c57e0-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="c57e0-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c57e0-132">-LoadBalancer</span></span>
<span data-ttu-id="c57e0-133">Referensen för belastnings Utjämnings resursen.</span><span class="sxs-lookup"><span data-stu-id="c57e0-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="c57e0-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="c57e0-134">-Name</span></span>
<span data-ttu-id="c57e0-135">Namn på regeln för utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="c57e0-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="c57e0-136">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="c57e0-136">-Protocol</span></span>
<span data-ttu-id="c57e0-137">Protokoll – TCP, UDP eller alla</span><span class="sxs-lookup"><span data-stu-id="c57e0-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="c57e0-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c57e0-138">-Confirm</span></span>
<span data-ttu-id="c57e0-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c57e0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c57e0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c57e0-140">-WhatIf</span></span>
<span data-ttu-id="c57e0-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c57e0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c57e0-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c57e0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c57e0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c57e0-143">CommonParameters</span></span>
<span data-ttu-id="c57e0-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c57e0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c57e0-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c57e0-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c57e0-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c57e0-146">INPUTS</span></span>

### <span data-ttu-id="c57e0-147">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c57e0-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="c57e0-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c57e0-148">System.Int32</span></span>

### <span data-ttu-id="c57e0-149">System. String</span><span class="sxs-lookup"><span data-stu-id="c57e0-149">System.String</span></span>

### <span data-ttu-id="c57e0-150">Microsoft. Azure. commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="c57e0-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="c57e0-151">Microsoft. Azure. commands. Networks. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c57e0-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="c57e0-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c57e0-152">OUTPUTS</span></span>

### <span data-ttu-id="c57e0-153">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c57e0-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c57e0-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c57e0-154">NOTES</span></span>

## <span data-ttu-id="c57e0-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c57e0-155">RELATED LINKS</span></span>

[<span data-ttu-id="c57e0-156">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c57e0-156">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c57e0-157">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c57e0-157">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c57e0-158">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c57e0-158">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c57e0-159">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c57e0-159">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)
