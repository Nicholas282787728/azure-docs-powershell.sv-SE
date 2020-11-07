---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: f566c2b9ac771071a9eb72673edb7e5218656c9b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924198"
---
# <span data-ttu-id="9c88e-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9c88e-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="9c88e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c88e-102">SYNOPSIS</span></span>
<span data-ttu-id="9c88e-103">Anger mål tillstånd för en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="9c88e-103">Sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="9c88e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c88e-104">SYNTAX</span></span>

### <span data-ttu-id="9c88e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9c88e-105">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c88e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9c88e-106">SetByResource</span></span>
```
Set-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c88e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c88e-107">DESCRIPTION</span></span>
<span data-ttu-id="9c88e-108">Cmdleten **set-AzLoadBalancerRuleConfig** anger mål tillstånd för en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="9c88e-108">The **Set-AzLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="9c88e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c88e-109">EXAMPLES</span></span>

### <span data-ttu-id="9c88e-110">Exempel 1: ändra en regel för belastnings Utjämnings regler</span><span class="sxs-lookup"><span data-stu-id="9c88e-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="9c88e-111">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i $slb variabel.</span><span class="sxs-lookup"><span data-stu-id="9c88e-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="9c88e-112">I det andra kommandot används pipeline-operatorn för att överföra belastningsutjämnaren i $slb till Add-AzLoadBalancerRuleConfig, som lägger till en regel som heter NewRule.</span><span class="sxs-lookup"><span data-stu-id="9c88e-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>

<span data-ttu-id="9c88e-113">Det tredje kommandot skickar belastningsutjämnaren till **set-AzLoadBalancerRuleConfig** , som anger den nya regel konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="9c88e-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="9c88e-114">Observera att konfigurationen inte aktiverar en flytande IP-adress, som har Aktiver ATS av föregående kommando.</span><span class="sxs-lookup"><span data-stu-id="9c88e-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="9c88e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c88e-115">PARAMETERS</span></span>

### <span data-ttu-id="9c88e-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9c88e-116">-BackendAddressPool</span></span>
<span data-ttu-id="9c88e-117">Anger ett **BackendAddressPool** -objekt som ska kopplas till en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="9c88e-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="9c88e-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9c88e-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="9c88e-119">Anger ID för ett **BackendAddressPool** -objekt som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="9c88e-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9c88e-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="9c88e-120">-BackendPort</span></span>
<span data-ttu-id="9c88e-121">Anger Server dels porten för trafik som matchas av denna regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9c88e-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="9c88e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c88e-122">-DefaultProfile</span></span>
<span data-ttu-id="9c88e-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c88e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c88e-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="9c88e-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="9c88e-125">Konfigurerar SNAT för de virtuella datorerna i backend-poolen till att använda den publicIP-adress som anges i klient delen av regeln för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="9c88e-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="9c88e-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="9c88e-126">-EnableFloatingIP</span></span>
<span data-ttu-id="9c88e-127">Anger att denna cmdlet aktiverar en flytande IP-adress för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9c88e-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="9c88e-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c88e-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="9c88e-129">Anger en lista över de front-IP-adresser som är associerade med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="9c88e-129">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9c88e-130">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9c88e-130">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="9c88e-131">Anger ID för en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="9c88e-131">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="9c88e-132">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="9c88e-132">-FrontendPort</span></span>
<span data-ttu-id="9c88e-133">Anger front porten som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="9c88e-133">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9c88e-134">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="9c88e-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="9c88e-135">Anger hur lång tid, i minuter, som status för konversationer ska behållas i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="9c88e-135">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="9c88e-136">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9c88e-136">-LoadBalancer</span></span>
<span data-ttu-id="9c88e-137">Anger en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="9c88e-137">Specifies a load balancer.</span></span>
<span data-ttu-id="9c88e-138">Denna cmdlet anger regel konfigurationen för mål tillstånd för belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9c88e-138">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="9c88e-139">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="9c88e-139">-LoadDistribution</span></span>
<span data-ttu-id="9c88e-140">Anger en belastnings fördelning.</span><span class="sxs-lookup"><span data-stu-id="9c88e-140">Specifies a load distribution.</span></span>
<span data-ttu-id="9c88e-141">De acceptabla värdena för den här parametern är: SourceIP och SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="9c88e-141">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="9c88e-142">-Namn</span><span class="sxs-lookup"><span data-stu-id="9c88e-142">-Name</span></span>
<span data-ttu-id="9c88e-143">Anger namnet på en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="9c88e-143">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="9c88e-144">-Sond</span><span class="sxs-lookup"><span data-stu-id="9c88e-144">-Probe</span></span>
<span data-ttu-id="9c88e-145">Anger en sond som associeras med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="9c88e-145">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9c88e-146">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="9c88e-146">-ProbeId</span></span>
<span data-ttu-id="9c88e-147">Anger ID för den sond som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="9c88e-147">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9c88e-148">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="9c88e-148">-Protocol</span></span>
<span data-ttu-id="9c88e-149">Anger det protokoll som matchas med en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="9c88e-149">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="9c88e-150">De acceptabla värdena för denna parameter är: TCP eller UDP.</span><span class="sxs-lookup"><span data-stu-id="9c88e-150">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="9c88e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c88e-151">CommonParameters</span></span>
<span data-ttu-id="9c88e-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c88e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c88e-153">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c88e-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c88e-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c88e-154">INPUTS</span></span>

### <span data-ttu-id="9c88e-155">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9c88e-155">PSLoadBalancer</span></span>
<span data-ttu-id="9c88e-156">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9c88e-156">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="9c88e-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c88e-157">OUTPUTS</span></span>

### <span data-ttu-id="9c88e-158">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9c88e-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9c88e-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c88e-159">NOTES</span></span>

## <span data-ttu-id="9c88e-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c88e-160">RELATED LINKS</span></span>

[<span data-ttu-id="9c88e-161">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9c88e-161">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="9c88e-162">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9c88e-162">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="9c88e-163">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9c88e-163">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="9c88e-164">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9c88e-164">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="9c88e-165">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9c88e-165">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)


