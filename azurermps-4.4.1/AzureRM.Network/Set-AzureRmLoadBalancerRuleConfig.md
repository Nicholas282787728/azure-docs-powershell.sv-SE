---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 2b9c835e99a088a075656cd985004663e5ef094a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575971"
---
# <span data-ttu-id="e5c1d-101">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e5c1d-101">Set-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="e5c1d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5c1d-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c1d-103">Anger mål tillstånd för en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-103">Sets the goal state for a load balancer rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5c1d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5c1d-104">SYNTAX</span></span>

### <span data-ttu-id="e5c1d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5c1d-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5c1d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e5c1d-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5c1d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5c1d-107">DESCRIPTION</span></span>
<span data-ttu-id="e5c1d-108">Cmdleten **set-AzureRmLoadBalancerRuleConfig** anger mål tillstånd för en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-108">The **Set-AzureRmLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="e5c1d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5c1d-109">EXAMPLES</span></span>

### <span data-ttu-id="e5c1d-110">Exempel 1: ändra en regel för belastnings Utjämnings regler</span><span class="sxs-lookup"><span data-stu-id="e5c1d-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="e5c1d-111">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i $slb variabel.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="e5c1d-112">I det andra kommandot används pipeline-operatorn för att överföra belastningsutjämnaren i $slb till Add-AzureRmLoadBalancerRuleConfig, som lägger till en regel som heter NewRule.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>

<span data-ttu-id="e5c1d-113">Det tredje kommandot skickar belastningsutjämnaren till **set-AzureRmLoadBalancerRuleConfig** , som anger den nya regel konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="e5c1d-114">Observera att konfigurationen inte aktiverar en flytande IP-adress, som har Aktiver ATS av föregående kommando.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="e5c1d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5c1d-115">PARAMETERS</span></span>

### <span data-ttu-id="e5c1d-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e5c1d-116">-BackendAddressPool</span></span>
<span data-ttu-id="e5c1d-117">Anger ett **BackendAddressPool** -objekt som ska kopplas till en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c1d-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e5c1d-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="e5c1d-119">Anger ID för ett **BackendAddressPool** -objekt som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e5c1d-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="e5c1d-120">-BackendPort</span></span>
<span data-ttu-id="e5c1d-121">Anger Server dels porten för trafik som matchas av denna regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="e5c1d-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="e5c1d-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="e5c1d-123">Konfigurerar SNAT för de virtuella datorerna i backend-poolen till att använda den publicIP-adress som anges i klient delen av regeln för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="e5c1d-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="e5c1d-124">-EnableFloatingIP</span></span>
<span data-ttu-id="e5c1d-125">Anger att denna cmdlet aktiverar en flytande IP-adress för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="e5c1d-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5c1d-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="e5c1d-127">Anger en lista över de front-IP-adresser som är associerade med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e5c1d-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e5c1d-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="e5c1d-129">Anger ID för en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="e5c1d-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="e5c1d-130">-FrontendPort</span></span>
<span data-ttu-id="e5c1d-131">Anger front porten som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e5c1d-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="e5c1d-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="e5c1d-133">Anger hur lång tid, i minuter, som status för konversationer ska behållas i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="e5c1d-134">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e5c1d-134">-LoadBalancer</span></span>
<span data-ttu-id="e5c1d-135">Anger en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-135">Specifies a load balancer.</span></span>
<span data-ttu-id="e5c1d-136">Denna cmdlet anger regel konfigurationen för mål tillstånd för belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-136">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="e5c1d-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="e5c1d-137">-LoadDistribution</span></span>
<span data-ttu-id="e5c1d-138">Anger en belastnings fördelning.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-138">Specifies a load distribution.</span></span>
<span data-ttu-id="e5c1d-139">De acceptabla värdena för den här parametern är: SourceIP och SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-139">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Default, SourceIP, SourceIPProtocol

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c1d-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="e5c1d-140">-Name</span></span>
<span data-ttu-id="e5c1d-141">Anger namnet på en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-141">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="e5c1d-142">-Sond</span><span class="sxs-lookup"><span data-stu-id="e5c1d-142">-Probe</span></span>
<span data-ttu-id="e5c1d-143">Anger en sond som associeras med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c1d-144">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="e5c1d-144">-ProbeId</span></span>
<span data-ttu-id="e5c1d-145">Anger ID för den sond som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e5c1d-146">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="e5c1d-146">-Protocol</span></span>
<span data-ttu-id="e5c1d-147">Anger det protokoll som matchas med en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-147">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="e5c1d-148">De acceptabla värdena för denna parameter är: TCP eller UDP.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="e5c1d-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c1d-149">-DefaultProfile</span></span>
<span data-ttu-id="e5c1d-150">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5c1d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c1d-151">CommonParameters</span></span>
<span data-ttu-id="e5c1d-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5c1d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c1d-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5c1d-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c1d-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5c1d-154">INPUTS</span></span>

### <span data-ttu-id="e5c1d-155">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e5c1d-155">PSLoadBalancer</span></span>
<span data-ttu-id="e5c1d-156">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e5c1d-156">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="e5c1d-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5c1d-157">OUTPUTS</span></span>

### <span data-ttu-id="e5c1d-158">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e5c1d-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e5c1d-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5c1d-159">NOTES</span></span>

## <span data-ttu-id="e5c1d-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5c1d-160">RELATED LINKS</span></span>

[<span data-ttu-id="e5c1d-161">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e5c1d-161">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="e5c1d-162">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e5c1d-162">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="e5c1d-163">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e5c1d-163">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="e5c1d-164">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e5c1d-164">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="e5c1d-165">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e5c1d-165">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)


