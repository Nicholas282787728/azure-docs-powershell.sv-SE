---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 004180f2369616654741df960a56a9f9c5bb6047
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575981"
---
# <span data-ttu-id="f5b46-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5b46-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="f5b46-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5b46-102">SYNOPSIS</span></span>
<span data-ttu-id="f5b46-103">Anger en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="f5b46-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5b46-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5b46-104">SYNTAX</span></span>

### <span data-ttu-id="f5b46-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f5b46-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5b46-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f5b46-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5b46-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5b46-107">DESCRIPTION</span></span>
<span data-ttu-id="f5b46-108">Cmdleten **set-AzureRmLoadBalancerInboundNatRuleConfig** anger en regel för inkommande NAT-regler (Network Address Translation) för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="f5b46-108">The **Set-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="f5b46-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5b46-109">EXAMPLES</span></span>

### <span data-ttu-id="f5b46-110">Exempel 1: ändra konfigurationen för inkommande NAT-regler på en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="f5b46-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="f5b46-111">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i $slb variabel.</span><span class="sxs-lookup"><span data-stu-id="f5b46-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="f5b46-112">Det andra kommandot använder pipeline-operatorn för att överföra belastningsutjämnaren i $slb till Add-AzureRmLoadBalancerInboundNatRuleConfig, vilket lägger till en inkommande NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="f5b46-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>

<span data-ttu-id="f5b46-113">Det tredje kommandot skickar belastningsutjämnaren till **set-AzureRmLoadBalancerInboundNatRuleConfig** , som sparar och uppdaterar den inkommande NAT-regelns konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f5b46-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="f5b46-114">Observera att regel konfigurationen har ställts in utan att aktivera flytande IP, som har Aktiver ATS med föregående kommando.</span><span class="sxs-lookup"><span data-stu-id="f5b46-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="f5b46-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5b46-115">PARAMETERS</span></span>

### <span data-ttu-id="f5b46-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="f5b46-116">-BackendPort</span></span>
<span data-ttu-id="f5b46-117">Anger Server dels porten för trafik som matchas av denna regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f5b46-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="f5b46-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="f5b46-118">-EnableFloatingIP</span></span>
<span data-ttu-id="f5b46-119">Anger att denna cmdlet aktiverar en flytande IP-adress för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f5b46-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="f5b46-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5b46-120">-FrontendIpConfiguration</span></span>
<span data-ttu-id="f5b46-121">Anger en lista med IP-adresser som ska kopplas till en inkommande NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="f5b46-121">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="f5b46-122">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f5b46-122">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="f5b46-123">Anger ID för en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f5b46-123">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="f5b46-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="f5b46-124">-FrontendPort</span></span>
<span data-ttu-id="f5b46-125">Anger front porten som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="f5b46-125">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f5b46-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f5b46-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="f5b46-127">Anger hur lång tid, i minuter, som status för konversationer ska behållas i en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="f5b46-127">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="f5b46-128">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f5b46-128">-LoadBalancer</span></span>
<span data-ttu-id="f5b46-129">Anger en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="f5b46-129">Specifies a load balancer.</span></span>
<span data-ttu-id="f5b46-130">Denna cmdlet anger en inkommande NAT-regel för belastnings utjämning som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f5b46-130">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5b46-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="f5b46-131">-Name</span></span>
<span data-ttu-id="f5b46-132">Anger namnet på en inkommande NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="f5b46-132">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="f5b46-133">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="f5b46-133">-Protocol</span></span>
<span data-ttu-id="f5b46-134">Anger det protokoll som matchas av en inkommande NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="f5b46-134">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="f5b46-135">De acceptabla värdena för denna parameter är: TCP eller UDP.</span><span class="sxs-lookup"><span data-stu-id="f5b46-135">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="f5b46-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5b46-136">-DefaultProfile</span></span>
<span data-ttu-id="f5b46-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f5b46-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5b46-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5b46-138">CommonParameters</span></span>
<span data-ttu-id="f5b46-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5b46-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5b46-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5b46-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5b46-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5b46-141">INPUTS</span></span>

### <span data-ttu-id="f5b46-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f5b46-142">PSLoadBalancer</span></span>
<span data-ttu-id="f5b46-143">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f5b46-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="f5b46-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5b46-144">OUTPUTS</span></span>

### <span data-ttu-id="f5b46-145">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f5b46-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f5b46-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5b46-146">NOTES</span></span>

## <span data-ttu-id="f5b46-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5b46-147">RELATED LINKS</span></span>

[<span data-ttu-id="f5b46-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5b46-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f5b46-149">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f5b46-149">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="f5b46-150">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5b46-150">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f5b46-151">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5b46-151">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f5b46-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5b46-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)


