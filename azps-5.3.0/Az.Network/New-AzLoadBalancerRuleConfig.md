---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 0a23cec7a2006e2e30a60a722deef14704a4d2c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523869"
---
# <span data-ttu-id="5803a-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5803a-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="5803a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5803a-102">SYNOPSIS</span></span>
<span data-ttu-id="5803a-103">Skapar en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="5803a-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="5803a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5803a-104">SYNTAX</span></span>

### <span data-ttu-id="5803a-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="5803a-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5803a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5803a-106">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5803a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5803a-107">DESCRIPTION</span></span>
<span data-ttu-id="5803a-108">Cmdleten **New-AzLoadBalancerRuleConfig** skapar en regel konfiguration för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="5803a-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="5803a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5803a-109">EXAMPLES</span></span>

### <span data-ttu-id="5803a-110">Exempel 1: skapa en regel konfiguration för en Azure-belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="5803a-110">Example 1: Creating a rule configuration for an Azure Load Balancer</span></span>
```powershell
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" `
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd `
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port `
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration `
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp `
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP `
    -LoadDistribution SourceIP
```

<span data-ttu-id="5803a-111">De första tre kommandona konfigurera en offentlig IP-adress, en klient del och en avsökning för regel konfigurationen i det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="5803a-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="5803a-112">Med kommandot tillbaka skapas en ny regel som heter MyLBrule med vissa specifikationer.</span><span class="sxs-lookup"><span data-stu-id="5803a-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="5803a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5803a-113">PARAMETERS</span></span>

### <span data-ttu-id="5803a-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5803a-114">-BackendAddressPool</span></span>
<span data-ttu-id="5803a-115">Anger ett **BackendAddressPool** -objekt som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="5803a-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="5803a-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="5803a-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="5803a-117">Anger ID för ett **BackendAddressPool** -objekt som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="5803a-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="5803a-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="5803a-118">-BackendPort</span></span>
<span data-ttu-id="5803a-119">Anger Server dels porten för trafik som matchas av denna regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="5803a-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="5803a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5803a-120">-DefaultProfile</span></span>
<span data-ttu-id="5803a-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5803a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5803a-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="5803a-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="5803a-123">Konfigurerar SNAT för de virtuella datorerna i backend-poolen till att använda den publicIP-adress som anges i klient delen av regeln för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="5803a-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="5803a-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="5803a-124">-EnableFloatingIP</span></span>
<span data-ttu-id="5803a-125">Anger att denna cmdlet aktiverar en flytande IP-adress för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5803a-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="5803a-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="5803a-126">-EnableTcpReset</span></span>
<span data-ttu-id="5803a-127">Ta emot dubbelriktad TCP-återställning i TCP-flödets tids gräns för inaktivitet eller oväntat upphör Ande.</span><span class="sxs-lookup"><span data-stu-id="5803a-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="5803a-128">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="5803a-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="5803a-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5803a-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="5803a-130">Anger en lista över de front-IP-adresser som är associerade med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="5803a-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="5803a-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5803a-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="5803a-132">Anger ID för en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="5803a-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="5803a-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="5803a-133">-FrontendPort</span></span>
<span data-ttu-id="5803a-134">Anger front porten som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="5803a-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="5803a-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="5803a-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="5803a-136">Anger hur lång tid, i minuter, som status för konversationer ska behållas i en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="5803a-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="5803a-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="5803a-137">-LoadDistribution</span></span>
<span data-ttu-id="5803a-138">Anger en belastnings fördelning.</span><span class="sxs-lookup"><span data-stu-id="5803a-138">Specifies a load distribution.</span></span>
<span data-ttu-id="5803a-139">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="5803a-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5803a-140">Vis</span><span class="sxs-lookup"><span data-stu-id="5803a-140">Default</span></span>
- <span data-ttu-id="5803a-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="5803a-141">SourceIP</span></span>
- <span data-ttu-id="5803a-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="5803a-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="5803a-143">-Namn</span><span class="sxs-lookup"><span data-stu-id="5803a-143">-Name</span></span>
<span data-ttu-id="5803a-144">Anger namnet på den regler för belastnings utjämning som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="5803a-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5803a-145">-Sond</span><span class="sxs-lookup"><span data-stu-id="5803a-145">-Probe</span></span>
<span data-ttu-id="5803a-146">Anger en sond som associeras med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="5803a-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="5803a-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="5803a-147">-ProbeId</span></span>
<span data-ttu-id="5803a-148">Anger ID för den sond som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="5803a-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="5803a-149">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="5803a-149">-Protocol</span></span>
<span data-ttu-id="5803a-150">Anger det protokoll som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="5803a-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="5803a-151">De acceptabla värdena för denna parameter är: TCP eller UDP.</span><span class="sxs-lookup"><span data-stu-id="5803a-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="5803a-152">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5803a-152">-Confirm</span></span>
<span data-ttu-id="5803a-153">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5803a-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5803a-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5803a-154">-WhatIf</span></span>
<span data-ttu-id="5803a-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5803a-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5803a-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5803a-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5803a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5803a-157">CommonParameters</span></span>
<span data-ttu-id="5803a-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5803a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5803a-159">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5803a-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5803a-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5803a-160">INPUTS</span></span>

### <span data-ttu-id="5803a-161">System. String</span><span class="sxs-lookup"><span data-stu-id="5803a-161">System.String</span></span>

### <span data-ttu-id="5803a-162">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5803a-162">System.Int32</span></span>

### <span data-ttu-id="5803a-163">Microsoft. Azure. commands. Networks. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5803a-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="5803a-164">Microsoft. Azure. commands. Networks. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5803a-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="5803a-165">Microsoft. Azure. commands. Networks. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="5803a-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="5803a-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5803a-166">OUTPUTS</span></span>

### <span data-ttu-id="5803a-167">Microsoft. Azure. commands. Networks. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="5803a-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="5803a-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5803a-168">NOTES</span></span>

## <span data-ttu-id="5803a-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5803a-169">RELATED LINKS</span></span>

[<span data-ttu-id="5803a-170">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5803a-170">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="5803a-171">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5803a-171">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="5803a-172">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5803a-172">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="5803a-173">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5803a-173">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


