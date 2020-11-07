---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6a699907b70256995973bfdbde4e11b08c594669
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922402"
---
# <span data-ttu-id="033e0-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="033e0-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="033e0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="033e0-102">SYNOPSIS</span></span>
<span data-ttu-id="033e0-103">Lägger till en inkommande NAT-regel i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="033e0-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="033e0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="033e0-104">SYNTAX</span></span>

### <span data-ttu-id="033e0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="033e0-105">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="033e0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="033e0-106">SetByResource</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="033e0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="033e0-107">DESCRIPTION</span></span>
<span data-ttu-id="033e0-108">Cmdleten **Add-AzLoadBalancerInboundNatRuleConfig** lägger till en inkommande NAT-regel (Network Address Translation) för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="033e0-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="033e0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="033e0-109">EXAMPLES</span></span>

### <span data-ttu-id="033e0-110">Exempel 1: lägga till en inkommande NAT-regel i en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="033e0-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="033e0-111">Det första kommandot får belastningsutjämnaren med namnet MyloadBalancer och lagrar det sedan i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="033e0-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="033e0-112">I det andra kommandot används pipeline-operatorn för att överföra belastningsutjämnaren i $slb till **Add-AzLoadBalancerInboundNatRuleConfig** , som lägger till en regel för inkommande NAT-regler till belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="033e0-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="033e0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="033e0-113">PARAMETERS</span></span>

### <span data-ttu-id="033e0-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="033e0-114">-BackendPort</span></span>
<span data-ttu-id="033e0-115">Anger backend-porten för trafik som matchas av en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="033e0-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="033e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="033e0-116">-DefaultProfile</span></span>
<span data-ttu-id="033e0-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="033e0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="033e0-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="033e0-118">-EnableFloatingIP</span></span>
<span data-ttu-id="033e0-119">Anger att denna cmdlet aktiverar en flytande IP-adress för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="033e0-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="033e0-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="033e0-120">-FrontendIpConfiguration</span></span>
<span data-ttu-id="033e0-121">Anger en lista med IP-adresser som ska kopplas till en inkommande NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="033e0-121">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="033e0-122">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="033e0-122">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="033e0-123">Anger ett ID för en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="033e0-123">Specifies an ID for a front-end IP address configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="033e0-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="033e0-124">-FrontendPort</span></span>
<span data-ttu-id="033e0-125">Anger front porten som matchas av en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="033e0-125">Specifies the front-end port that is matched by a rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="033e0-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="033e0-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="033e0-127">Anger hur lång tid, i minuter, som status för konversationer ska behållas i en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="033e0-127">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="033e0-128">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="033e0-128">-LoadBalancer</span></span>
<span data-ttu-id="033e0-129">Anger ett **Loadbalancer** -objekt.</span><span class="sxs-lookup"><span data-stu-id="033e0-129">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="033e0-130">Denna cmdlet lägger till en inkommande NAT-regel för belastnings utjämning som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="033e0-130">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="033e0-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="033e0-131">-Name</span></span>
<span data-ttu-id="033e0-132">Anger namnet på den inkommande NAT-regelns konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="033e0-132">Specifies the name of the inbound NAT rule configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="033e0-133">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="033e0-133">-Protocol</span></span>
<span data-ttu-id="033e0-134">Anger det protokoll som matchas av en inkommande NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="033e0-134">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="033e0-135">De acceptabla värdena för denna parameter är: TCP eller UDP.</span><span class="sxs-lookup"><span data-stu-id="033e0-135">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="033e0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="033e0-136">CommonParameters</span></span>
<span data-ttu-id="033e0-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="033e0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="033e0-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="033e0-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="033e0-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="033e0-139">INPUTS</span></span>

### <span data-ttu-id="033e0-140">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="033e0-140">PSLoadBalancer</span></span>
<span data-ttu-id="033e0-141">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="033e0-141">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="033e0-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="033e0-142">OUTPUTS</span></span>

### <span data-ttu-id="033e0-143">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="033e0-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="033e0-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="033e0-144">NOTES</span></span>

## <span data-ttu-id="033e0-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="033e0-145">RELATED LINKS</span></span>

[<span data-ttu-id="033e0-146">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="033e0-146">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="033e0-147">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="033e0-147">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="033e0-148">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="033e0-148">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="033e0-149">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="033e0-149">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="033e0-150">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="033e0-150">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="033e0-151">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="033e0-151">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


