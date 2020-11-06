---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: ac96a07fb7ec32589ac351fc592c4c2848e75978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574816"
---
# <span data-ttu-id="2535f-101">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2535f-101">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="2535f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2535f-102">SYNOPSIS</span></span>
<span data-ttu-id="2535f-103">Lägger till en regel för utgående trafik till en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="2535f-103">Adds an outbound rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2535f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2535f-104">SYNTAX</span></span>

### <span data-ttu-id="2535f-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="2535f-105">SetByResource (Default)</span></span>
```
Add-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2535f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2535f-106">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2535f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2535f-107">DESCRIPTION</span></span>
<span data-ttu-id="2535f-108">Cmdleten **Add-AzureRmLoadBalancerOutboundRuleConfig** lägger till en regel för utgående trafik i en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="2535f-108">The **Add-AzureRmLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="2535f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2535f-109">EXAMPLES</span></span>

### <span data-ttu-id="2535f-110">Exempel 1: lägga till en regel för utgående trafik till en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="2535f-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzureRmLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="2535f-111">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="2535f-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="2535f-112">I det andra kommandot används pipeline-operatorn för att överföra belastningsutjämnaren i $slb till **Add-AzureRmLoadBalancerOutboundRuleConfig** , som lägger till en regel för utgående trafik till belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="2535f-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerOutboundRuleConfig** , which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="2535f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2535f-113">PARAMETERS</span></span>

### <span data-ttu-id="2535f-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="2535f-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="2535f-115">Antalet utgående portar som ska användas för NAT.</span><span class="sxs-lookup"><span data-stu-id="2535f-115">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="2535f-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2535f-116">-BackendAddressPool</span></span>
<span data-ttu-id="2535f-117">En referens till en pool med DIP.</span><span class="sxs-lookup"><span data-stu-id="2535f-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="2535f-118">Utgående trafik bal anse ras slumpmässigt för IP i Server delen.</span><span class="sxs-lookup"><span data-stu-id="2535f-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="2535f-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2535f-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="2535f-120">En referens till en pool med DIP.</span><span class="sxs-lookup"><span data-stu-id="2535f-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="2535f-121">Utgående trafik bal anse ras slumpmässigt för IP i Server delen.</span><span class="sxs-lookup"><span data-stu-id="2535f-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="2535f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2535f-122">-DefaultProfile</span></span>
<span data-ttu-id="2535f-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2535f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2535f-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="2535f-124">-EnableTcpReset</span></span>
<span data-ttu-id="2535f-125">Ta emot dubbelriktad TCP-återställning i TCP-flödets tids gräns för inaktivitet eller oväntat upphör Ande.</span><span class="sxs-lookup"><span data-stu-id="2535f-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="2535f-126">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="2535f-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="2535f-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2535f-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="2535f-128">Belastnings utjämningens IP-adresser för klient delen.</span><span class="sxs-lookup"><span data-stu-id="2535f-128">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2535f-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="2535f-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="2535f-130">Timeout för TCP-inaktiv anslutning</span><span class="sxs-lookup"><span data-stu-id="2535f-130">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="2535f-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2535f-131">-LoadBalancer</span></span>
<span data-ttu-id="2535f-132">Referensen för belastnings Utjämnings resursen.</span><span class="sxs-lookup"><span data-stu-id="2535f-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="2535f-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="2535f-133">-Name</span></span>
<span data-ttu-id="2535f-134">Namn på regeln för utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="2535f-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="2535f-135">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="2535f-135">-Protocol</span></span>
<span data-ttu-id="2535f-136">Protokoll – TCP, UDP eller alla</span><span class="sxs-lookup"><span data-stu-id="2535f-136">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="2535f-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2535f-137">-Confirm</span></span>
<span data-ttu-id="2535f-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2535f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2535f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2535f-139">-WhatIf</span></span>
<span data-ttu-id="2535f-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2535f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2535f-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2535f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2535f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2535f-142">CommonParameters</span></span>
<span data-ttu-id="2535f-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2535f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2535f-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2535f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2535f-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2535f-145">INPUTS</span></span>

### <span data-ttu-id="2535f-146">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2535f-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="2535f-147">System. Int32 system. String system. Collections. Generic. list \` 1 [[Microsoft. Azure. kommandon. Network. Models. PSResourceId, Microsoft. Azure. commands. Network, version = 6.5.0.0, Culture = neutralt, PublicKeyToken = null]] Microsoft. Azure. commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2535f-147">System.Int32 System.String System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSResourceId, Microsoft.Azure.Commands.Network, Version=6.5.0.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="2535f-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2535f-148">OUTPUTS</span></span>

### <span data-ttu-id="2535f-149">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2535f-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2535f-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2535f-150">NOTES</span></span>

## <span data-ttu-id="2535f-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2535f-151">RELATED LINKS</span></span>
