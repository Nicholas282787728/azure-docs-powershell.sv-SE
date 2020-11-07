---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: 0708540cbb0ccac2f445fc0692c3c91f9358213c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930550"
---
# <span data-ttu-id="e5ad2-101">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e5ad2-101">Add-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="e5ad2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="e5ad2-103">Lägger till en regel konfiguration i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-103">Adds a rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5ad2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5ad2-104">SYNTAX</span></span>

### <span data-ttu-id="e5ad2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5ad2-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5ad2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e5ad2-106">SetByResource</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5ad2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5ad2-107">DESCRIPTION</span></span>
<span data-ttu-id="e5ad2-108">Cmdleten **Add-AzureRmLoadBalancerRuleConfig** lägger till en regel konfiguration i en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-108">The **Add-AzureRmLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="e5ad2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5ad2-109">EXAMPLES</span></span>

### <span data-ttu-id="e5ad2-110">Exempel 1: lägga till en regel konfiguration i en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="e5ad2-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="e5ad2-111">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="e5ad2-112">I det andra kommandot används pipeline-operatorn för att överföra belastningsutjämnaren i $slb till **Add-AzureRmLoadBalancerRuleConfig** , som lägger till regel konfigurationen med namnet NewRule.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>

## <span data-ttu-id="e5ad2-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5ad2-113">PARAMETERS</span></span>

### <span data-ttu-id="e5ad2-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e5ad2-114">-BackendAddressPool</span></span>
<span data-ttu-id="e5ad2-115">Anger Server delens adresspool för att associera med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-115">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5ad2-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e5ad2-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="e5ad2-117">Anger ID för ett **BackendAddressPool** -objekt som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e5ad2-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="e5ad2-118">-BackendPort</span></span>
<span data-ttu-id="e5ad2-119">Anger Server dels porten för trafik som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-119">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e5ad2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5ad2-120">-DefaultProfile</span></span>
<span data-ttu-id="e5ad2-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5ad2-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="e5ad2-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="e5ad2-123">Konfigurerar SNAT för de virtuella datorerna i backend-poolen till att använda den publicIP-adress som anges i klient delen av regeln för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="e5ad2-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="e5ad2-124">-EnableFloatingIP</span></span>
<span data-ttu-id="e5ad2-125">Anger att denna cmdlet aktiverar en flytande IP-adress för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="e5ad2-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5ad2-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="e5ad2-127">Anger en lista över de front-IP-adresser som är associerade med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e5ad2-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e5ad2-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="e5ad2-129">Anger ID för en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="e5ad2-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="e5ad2-130">-FrontendPort</span></span>
<span data-ttu-id="e5ad2-131">Anger front porten som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e5ad2-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="e5ad2-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="e5ad2-133">Anger hur lång tid, i minuter, som status för konversationer ska behållas i belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-133">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="e5ad2-134">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e5ad2-134">-LoadBalancer</span></span>
<span data-ttu-id="e5ad2-135">Anger ett **Loadbalancer** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-135">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="e5ad2-136">Denna cmdlet lägger till en regel konfiguration i belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-136">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="e5ad2-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="e5ad2-137">-LoadDistribution</span></span>
<span data-ttu-id="e5ad2-138">Anger en belastnings fördelning.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-138">Specifies a load distribution.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Default, SourceIP, SourceIPProtocol

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5ad2-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="e5ad2-139">-Name</span></span>
<span data-ttu-id="e5ad2-140">Anger namnet på regeln för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-140">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e5ad2-141">-Sond</span><span class="sxs-lookup"><span data-stu-id="e5ad2-141">-Probe</span></span>
<span data-ttu-id="e5ad2-142">Anger en sond som associeras med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-142">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSProbe
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5ad2-143">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="e5ad2-143">-ProbeId</span></span>
<span data-ttu-id="e5ad2-144">Anger ID för den sond som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-144">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e5ad2-145">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="e5ad2-145">-Protocol</span></span>
<span data-ttu-id="e5ad2-146">Specfies protokollet som matchas med en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-146">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="e5ad2-147">De acceptabla värdena för denna parameter är: TCP eller UDP.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-147">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5ad2-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5ad2-148">CommonParameters</span></span>
<span data-ttu-id="e5ad2-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5ad2-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5ad2-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5ad2-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5ad2-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5ad2-151">INPUTS</span></span>

### <span data-ttu-id="e5ad2-152">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e5ad2-152">PSLoadBalancer</span></span>
<span data-ttu-id="e5ad2-153">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e5ad2-153">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="e5ad2-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5ad2-154">OUTPUTS</span></span>

### <span data-ttu-id="e5ad2-155">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e5ad2-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e5ad2-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5ad2-156">NOTES</span></span>

## <span data-ttu-id="e5ad2-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5ad2-157">RELATED LINKS</span></span>

[<span data-ttu-id="e5ad2-158">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e5ad2-158">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="e5ad2-159">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e5ad2-159">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="e5ad2-160">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e5ad2-160">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="e5ad2-161">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e5ad2-161">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="e5ad2-162">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e5ad2-162">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


