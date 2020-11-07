---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: ee0a001894570c66145ac7f75d12451df5faaab7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756336"
---
# <span data-ttu-id="5a332-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a332-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="5a332-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a332-102">SYNOPSIS</span></span>
<span data-ttu-id="5a332-103">Lägger till en inkommande NAT-regel i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="5a332-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a332-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a332-104">SYNTAX</span></span>

### <span data-ttu-id="5a332-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a332-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a332-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5a332-106">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a332-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a332-107">DESCRIPTION</span></span>
<span data-ttu-id="5a332-108">Cmdleten **Add-AzureRmLoadBalancerInboundNatRuleConfig** lägger till en inkommande NAT-regel (Network Address Translation) för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="5a332-108">The **Add-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="5a332-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a332-109">EXAMPLES</span></span>

### <span data-ttu-id="5a332-110">Exempel 1: lägga till en inkommande NAT-regel i en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="5a332-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="5a332-111">Det första kommandot får belastningsutjämnaren med namnet MyloadBalancer och lagrar det sedan i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="5a332-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="5a332-112">I det andra kommandot används pipeline-operatorn för att överföra belastningsutjämnaren i $slb till **Add-AzureRmLoadBalancerInboundNatRuleConfig** , som lägger till en regel för inkommande NAT-regler till belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="5a332-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="5a332-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a332-113">PARAMETERS</span></span>

### <span data-ttu-id="5a332-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="5a332-114">-BackendPort</span></span>
<span data-ttu-id="5a332-115">Anger backend-porten för trafik som matchas av en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5a332-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a332-116">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="5a332-116">-EnableFloatingIP</span></span>
<span data-ttu-id="5a332-117">Anger att denna cmdlet aktiverar en flytande IP-adress för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5a332-117">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="5a332-118">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a332-118">-FrontendIpConfiguration</span></span>
<span data-ttu-id="5a332-119">Anger en lista med IP-adresser som ska kopplas till en inkommande NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="5a332-119">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a332-120">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5a332-120">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="5a332-121">Anger ett ID för en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="5a332-121">Specifies an ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a332-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="5a332-122">-FrontendPort</span></span>
<span data-ttu-id="5a332-123">Anger front porten som matchas av en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5a332-123">Specifies the front-end port that is matched by a rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a332-124">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="5a332-124">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="5a332-125">Anger hur lång tid, i minuter, som status för konversationer ska behållas i en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="5a332-125">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a332-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5a332-126">-LoadBalancer</span></span>
<span data-ttu-id="5a332-127">Anger ett **Loadbalancer** -objekt.</span><span class="sxs-lookup"><span data-stu-id="5a332-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="5a332-128">Denna cmdlet lägger till en inkommande NAT-regel för belastnings utjämning som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="5a332-128">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a332-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="5a332-129">-Name</span></span>
<span data-ttu-id="5a332-130">Anger namnet på den inkommande NAT-regelns konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="5a332-130">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="5a332-131">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="5a332-131">-Protocol</span></span>
<span data-ttu-id="5a332-132">Anger det protokoll som matchas av en inkommande NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="5a332-132">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="5a332-133">De acceptabla värdena för denna parameter är: TCP eller UDP.</span><span class="sxs-lookup"><span data-stu-id="5a332-133">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a332-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a332-134">-DefaultProfile</span></span>
<span data-ttu-id="5a332-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5a332-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a332-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a332-136">CommonParameters</span></span>
<span data-ttu-id="5a332-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a332-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a332-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a332-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a332-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a332-139">INPUTS</span></span>

### <span data-ttu-id="5a332-140">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5a332-140">PSLoadBalancer</span></span>
<span data-ttu-id="5a332-141">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="5a332-141">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="5a332-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a332-142">OUTPUTS</span></span>

### <span data-ttu-id="5a332-143">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5a332-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5a332-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a332-144">NOTES</span></span>

## <span data-ttu-id="5a332-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a332-145">RELATED LINKS</span></span>

[<span data-ttu-id="5a332-146">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5a332-146">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="5a332-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a332-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="5a332-148">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a332-148">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="5a332-149">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a332-149">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="5a332-150">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5a332-150">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="5a332-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a332-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


