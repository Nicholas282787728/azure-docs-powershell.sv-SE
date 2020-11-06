---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: a584d473354fd900b117f5661dc738b239f3a92d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578871"
---
# <span data-ttu-id="c5fcc-101">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c5fcc-101">Set-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="c5fcc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c5fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="c5fcc-103">Anger mål tillstånd för en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-103">Sets the goal state for a load balancer rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5fcc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c5fcc-104">SYNTAX</span></span>

### <span data-ttu-id="c5fcc-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="c5fcc-105">SetByResource (Default)</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5fcc-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c5fcc-106">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5fcc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c5fcc-107">DESCRIPTION</span></span>
<span data-ttu-id="c5fcc-108">Cmdleten **set-AzureRmLoadBalancerRuleConfig** anger mål tillstånd för en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-108">The **Set-AzureRmLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="c5fcc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c5fcc-109">EXAMPLES</span></span>

### <span data-ttu-id="c5fcc-110">Exempel 1: ändra en regel för belastnings Utjämnings regler</span><span class="sxs-lookup"><span data-stu-id="c5fcc-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="c5fcc-111">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i $slb variabel.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="c5fcc-112">I det andra kommandot används pipeline-operatorn för att överföra belastningsutjämnaren i $slb till Add-AzureRmLoadBalancerRuleConfig, som lägger till en regel som heter NewRule.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="c5fcc-113">Det tredje kommandot skickar belastningsutjämnaren till **set-AzureRmLoadBalancerRuleConfig** , som anger den nya regel konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="c5fcc-114">Observera att konfigurationen inte aktiverar en flytande IP-adress, som har Aktiver ATS av föregående kommando.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="c5fcc-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c5fcc-115">PARAMETERS</span></span>

### <span data-ttu-id="c5fcc-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c5fcc-116">-BackendAddressPool</span></span>
<span data-ttu-id="c5fcc-117">Anger ett **BackendAddressPool** -objekt som ska kopplas till en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5fcc-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c5fcc-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="c5fcc-119">Anger ID för ett **BackendAddressPool** -objekt som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c5fcc-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="c5fcc-120">-BackendPort</span></span>
<span data-ttu-id="c5fcc-121">Anger Server dels porten för trafik som matchas av denna regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="c5fcc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5fcc-122">-DefaultProfile</span></span>
<span data-ttu-id="c5fcc-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5fcc-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="c5fcc-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="c5fcc-125">Konfigurerar SNAT för de virtuella datorerna i backend-poolen till att använda den publicIP-adress som anges i klient delen av regeln för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="c5fcc-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="c5fcc-126">-EnableFloatingIP</span></span>
<span data-ttu-id="c5fcc-127">Anger att denna cmdlet aktiverar en flytande IP-adress för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="c5fcc-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c5fcc-128">-EnableTcpReset</span></span>
<span data-ttu-id="c5fcc-129">Ta emot dubbelriktad TCP-återställning i TCP-flödets tids gräns för inaktivitet eller oväntat upphör Ande.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="c5fcc-130">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c5fcc-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5fcc-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c5fcc-132">Anger en lista över de front-IP-adresser som är associerade med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c5fcc-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c5fcc-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="c5fcc-134">Anger ID för en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-134">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="c5fcc-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="c5fcc-135">-FrontendPort</span></span>
<span data-ttu-id="c5fcc-136">Anger front porten som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c5fcc-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c5fcc-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c5fcc-138">Anger hur lång tid, i minuter, som status för konversationer ska behållas i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="c5fcc-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c5fcc-139">-LoadBalancer</span></span>
<span data-ttu-id="c5fcc-140">Anger en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-140">Specifies a load balancer.</span></span>
<span data-ttu-id="c5fcc-141">Denna cmdlet anger regel konfigurationen för mål tillstånd för belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-141">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="c5fcc-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="c5fcc-142">-LoadDistribution</span></span>
<span data-ttu-id="c5fcc-143">Anger en belastnings fördelning.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-143">Specifies a load distribution.</span></span>
<span data-ttu-id="c5fcc-144">De acceptabla värdena för den här parametern är: SourceIP och SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="c5fcc-145">-Namn</span><span class="sxs-lookup"><span data-stu-id="c5fcc-145">-Name</span></span>
<span data-ttu-id="c5fcc-146">Anger namnet på en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="c5fcc-147">-Sond</span><span class="sxs-lookup"><span data-stu-id="c5fcc-147">-Probe</span></span>
<span data-ttu-id="c5fcc-148">Anger en sond som associeras med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5fcc-149">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="c5fcc-149">-ProbeId</span></span>
<span data-ttu-id="c5fcc-150">Anger ID för den sond som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c5fcc-151">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="c5fcc-151">-Protocol</span></span>
<span data-ttu-id="c5fcc-152">Anger det protokoll som matchas med en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="c5fcc-153">De acceptabla värdena för denna parameter är: TCP eller UDP.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="c5fcc-154">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c5fcc-154">-Confirm</span></span>
<span data-ttu-id="c5fcc-155">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5fcc-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5fcc-156">-WhatIf</span></span>
<span data-ttu-id="c5fcc-157">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5fcc-158">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5fcc-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5fcc-159">CommonParameters</span></span>
<span data-ttu-id="c5fcc-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5fcc-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5fcc-161">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5fcc-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5fcc-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c5fcc-162">INPUTS</span></span>

### <span data-ttu-id="c5fcc-163">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c5fcc-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="c5fcc-164">Parametrar: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c5fcc-164">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="c5fcc-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c5fcc-165">OUTPUTS</span></span>

### <span data-ttu-id="c5fcc-166">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c5fcc-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c5fcc-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c5fcc-167">NOTES</span></span>

## <span data-ttu-id="c5fcc-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c5fcc-168">RELATED LINKS</span></span>

[<span data-ttu-id="c5fcc-169">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c5fcc-169">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="c5fcc-170">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c5fcc-170">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="c5fcc-171">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c5fcc-171">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="c5fcc-172">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c5fcc-172">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="c5fcc-173">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c5fcc-173">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)


