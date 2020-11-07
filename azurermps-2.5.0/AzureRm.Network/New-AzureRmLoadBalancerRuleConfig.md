---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: f3e256def28dff292efc5ba4278dc4f56b3ec721
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931238"
---
# <span data-ttu-id="11a22-101">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11a22-101">New-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="11a22-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11a22-102">SYNOPSIS</span></span>
<span data-ttu-id="11a22-103">Skapar en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="11a22-103">Creates a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11a22-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11a22-104">SYNTAX</span></span>

### <span data-ttu-id="11a22-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="11a22-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11a22-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="11a22-106">SetByResource</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11a22-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11a22-107">DESCRIPTION</span></span>
<span data-ttu-id="11a22-108">Cmdleten **New-AzureRmLoadBalancerRuleConfig** skapar en regel konfiguration för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="11a22-108">The **New-AzureRmLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="11a22-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11a22-109">EXAMPLES</span></span>

### <span data-ttu-id="11a22-110">1: skapa en regel konfiguration för en Azure-belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="11a22-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzureRmLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzureRmLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="11a22-111">De första tre kommandona konfigurera en offentlig IP-adress, en klient del och en avsökning för regel konfigurationen i det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="11a22-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="11a22-112">Med kommandot tillbaka skapas en ny regel som heter MyLBrule med vissa specifikationer.</span><span class="sxs-lookup"><span data-stu-id="11a22-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="11a22-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11a22-113">PARAMETERS</span></span>

### <span data-ttu-id="11a22-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="11a22-114">-BackendAddressPool</span></span>
<span data-ttu-id="11a22-115">Anger ett **BackendAddressPool** -objekt som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="11a22-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="11a22-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="11a22-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="11a22-117">Anger ID för ett **BackendAddressPool** -objekt som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="11a22-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="11a22-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="11a22-118">-BackendPort</span></span>
<span data-ttu-id="11a22-119">Anger Server dels porten för trafik som matchas av denna regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="11a22-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="11a22-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11a22-120">-DefaultProfile</span></span>
<span data-ttu-id="11a22-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="11a22-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11a22-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="11a22-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="11a22-123">Konfigurerar SNAT för de virtuella datorerna i backend-poolen till att använda den publicIP-adress som anges i klient delen av regeln för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="11a22-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="11a22-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="11a22-124">-EnableFloatingIP</span></span>
<span data-ttu-id="11a22-125">Anger att denna cmdlet aktiverar en flytande IP-adress för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="11a22-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="11a22-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="11a22-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="11a22-127">Anger en lista över de front-IP-adresser som är associerade med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="11a22-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="11a22-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="11a22-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="11a22-129">Anger ID för en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="11a22-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="11a22-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="11a22-130">-FrontendPort</span></span>
<span data-ttu-id="11a22-131">Anger front porten som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="11a22-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="11a22-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="11a22-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="11a22-133">Anger hur lång tid, i minuter, som status för konversationer ska behållas i en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="11a22-133">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="11a22-134">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="11a22-134">-LoadDistribution</span></span>
<span data-ttu-id="11a22-135">Anger en belastnings fördelning.</span><span class="sxs-lookup"><span data-stu-id="11a22-135">Specifies a load distribution.</span></span>
<span data-ttu-id="11a22-136">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="11a22-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11a22-137">Vis</span><span class="sxs-lookup"><span data-stu-id="11a22-137">Default</span></span>
- <span data-ttu-id="11a22-138">SourceIP</span><span class="sxs-lookup"><span data-stu-id="11a22-138">SourceIP</span></span>
- <span data-ttu-id="11a22-139">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="11a22-139">SourceIPProtocol</span></span>

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

### <span data-ttu-id="11a22-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="11a22-140">-Name</span></span>
<span data-ttu-id="11a22-141">Anger namnet på den regler för belastnings utjämning som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="11a22-141">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="11a22-142">-Sond</span><span class="sxs-lookup"><span data-stu-id="11a22-142">-Probe</span></span>
<span data-ttu-id="11a22-143">Anger en sond som associeras med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="11a22-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="11a22-144">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="11a22-144">-ProbeId</span></span>
<span data-ttu-id="11a22-145">Anger ID för den sond som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="11a22-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="11a22-146">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="11a22-146">-Protocol</span></span>
<span data-ttu-id="11a22-147">Anger det protokoll som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="11a22-147">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="11a22-148">De acceptabla värdena för denna parameter är: TCP eller UDP.</span><span class="sxs-lookup"><span data-stu-id="11a22-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="11a22-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11a22-149">CommonParameters</span></span>
<span data-ttu-id="11a22-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11a22-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11a22-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11a22-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11a22-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11a22-152">INPUTS</span></span>

## <span data-ttu-id="11a22-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11a22-153">OUTPUTS</span></span>

### <span data-ttu-id="11a22-154">Microsoft. Azure. commands. Networks. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="11a22-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="11a22-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11a22-155">NOTES</span></span>

## <span data-ttu-id="11a22-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11a22-156">RELATED LINKS</span></span>

[<span data-ttu-id="11a22-157">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11a22-157">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="11a22-158">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11a22-158">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="11a22-159">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11a22-159">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="11a22-160">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11a22-160">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


