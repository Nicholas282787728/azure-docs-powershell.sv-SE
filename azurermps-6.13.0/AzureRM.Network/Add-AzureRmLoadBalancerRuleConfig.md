---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 5ed21aec1be522ac145fe255065b650ca4c09dcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758177"
---
# <span data-ttu-id="887f4-101">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="887f4-101">Add-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="887f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="887f4-102">SYNOPSIS</span></span>
<span data-ttu-id="887f4-103">Lägger till en regel konfiguration i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="887f4-103">Adds a rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="887f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="887f4-104">SYNTAX</span></span>

### <span data-ttu-id="887f4-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="887f4-105">SetByResource (Default)</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="887f4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="887f4-106">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="887f4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="887f4-107">DESCRIPTION</span></span>
<span data-ttu-id="887f4-108">Cmdleten **Add-AzureRmLoadBalancerRuleConfig** lägger till en regel konfiguration i en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="887f4-108">The **Add-AzureRmLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="887f4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="887f4-109">EXAMPLES</span></span>

### <span data-ttu-id="887f4-110">Exempel 1: lägga till en regel konfiguration i en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="887f4-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="887f4-111">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="887f4-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="887f4-112">I det andra kommandot används pipeline-operatorn för att överföra belastningsutjämnaren i $slb till **Add-AzureRmLoadBalancerRuleConfig** , som lägger till regel konfigurationen med namnet NewRule.</span><span class="sxs-lookup"><span data-stu-id="887f4-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>

## <span data-ttu-id="887f4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="887f4-113">PARAMETERS</span></span>

### <span data-ttu-id="887f4-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="887f4-114">-BackendAddressPool</span></span>
<span data-ttu-id="887f4-115">Anger Server delens adresspool för att associera med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="887f4-115">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="887f4-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="887f4-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="887f4-117">Anger ID för ett **BackendAddressPool** -objekt som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="887f4-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="887f4-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="887f4-118">-BackendPort</span></span>
<span data-ttu-id="887f4-119">Anger Server dels porten för trafik som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="887f4-119">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="887f4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="887f4-120">-DefaultProfile</span></span>
<span data-ttu-id="887f4-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="887f4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="887f4-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="887f4-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="887f4-123">Konfigurerar SNAT för de virtuella datorerna i backend-poolen till att använda den publicIP-adress som anges i klient delen av regeln för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="887f4-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="887f4-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="887f4-124">-EnableFloatingIP</span></span>
<span data-ttu-id="887f4-125">Anger att denna cmdlet aktiverar en flytande IP-adress för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="887f4-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="887f4-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="887f4-126">-EnableTcpReset</span></span>
<span data-ttu-id="887f4-127">Ta emot dubbelriktad TCP-återställning i TCP-flödets tids gräns för inaktivitet eller oväntat upphör Ande.</span><span class="sxs-lookup"><span data-stu-id="887f4-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="887f4-128">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="887f4-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="887f4-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="887f4-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="887f4-130">Anger en lista över de front-IP-adresser som är associerade med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="887f4-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="887f4-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="887f4-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="887f4-132">Anger ID för en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="887f4-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="887f4-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="887f4-133">-FrontendPort</span></span>
<span data-ttu-id="887f4-134">Anger front porten som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="887f4-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="887f4-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="887f4-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="887f4-136">Anger hur lång tid, i minuter, som status för konversationer ska behållas i belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="887f4-136">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="887f4-137">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="887f4-137">-LoadBalancer</span></span>
<span data-ttu-id="887f4-138">Anger ett **Loadbalancer** -objekt.</span><span class="sxs-lookup"><span data-stu-id="887f4-138">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="887f4-139">Denna cmdlet lägger till en regel konfiguration i belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="887f4-139">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="887f4-140">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="887f4-140">-LoadDistribution</span></span>
<span data-ttu-id="887f4-141">Anger en belastnings fördelning.</span><span class="sxs-lookup"><span data-stu-id="887f4-141">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="887f4-142">-Namn</span><span class="sxs-lookup"><span data-stu-id="887f4-142">-Name</span></span>
<span data-ttu-id="887f4-143">Anger namnet på regeln för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="887f4-143">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="887f4-144">-Sond</span><span class="sxs-lookup"><span data-stu-id="887f4-144">-Probe</span></span>
<span data-ttu-id="887f4-145">Anger en sond som associeras med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="887f4-145">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="887f4-146">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="887f4-146">-ProbeId</span></span>
<span data-ttu-id="887f4-147">Anger ID för den sond som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="887f4-147">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="887f4-148">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="887f4-148">-Protocol</span></span>
<span data-ttu-id="887f4-149">Specfies protokollet som matchas med en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="887f4-149">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="887f4-150">De acceptabla värdena för denna parameter är: TCP eller UDP.</span><span class="sxs-lookup"><span data-stu-id="887f4-150">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="887f4-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="887f4-151">-Confirm</span></span>
<span data-ttu-id="887f4-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="887f4-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="887f4-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="887f4-153">-WhatIf</span></span>
<span data-ttu-id="887f4-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="887f4-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="887f4-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="887f4-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="887f4-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="887f4-156">CommonParameters</span></span>
<span data-ttu-id="887f4-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="887f4-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="887f4-158">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="887f4-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="887f4-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="887f4-159">INPUTS</span></span>

### <span data-ttu-id="887f4-160">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="887f4-160">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="887f4-161">Parametrar: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="887f4-161">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="887f4-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="887f4-162">OUTPUTS</span></span>

### <span data-ttu-id="887f4-163">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="887f4-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="887f4-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="887f4-164">NOTES</span></span>

## <span data-ttu-id="887f4-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="887f4-165">RELATED LINKS</span></span>

[<span data-ttu-id="887f4-166">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="887f4-166">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="887f4-167">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="887f4-167">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="887f4-168">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="887f4-168">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="887f4-169">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="887f4-169">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="887f4-170">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="887f4-170">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


