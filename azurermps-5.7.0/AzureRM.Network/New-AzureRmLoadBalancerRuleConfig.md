---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 076672dc8cb90126782b54c13ee99b41dff4ccbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756240"
---
# <span data-ttu-id="faf7c-101">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="faf7c-101">New-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="faf7c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="faf7c-102">SYNOPSIS</span></span>
<span data-ttu-id="faf7c-103">Skapar en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="faf7c-103">Creates a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faf7c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="faf7c-104">SYNTAX</span></span>

### <span data-ttu-id="faf7c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="faf7c-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="faf7c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="faf7c-106">SetByResource</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faf7c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="faf7c-107">DESCRIPTION</span></span>
<span data-ttu-id="faf7c-108">Cmdleten **New-AzureRmLoadBalancerRuleConfig** skapar en regel konfiguration för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="faf7c-108">The **New-AzureRmLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="faf7c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="faf7c-109">EXAMPLES</span></span>

### <span data-ttu-id="faf7c-110">1: skapa en regel konfiguration för en Azure-belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="faf7c-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
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

<span data-ttu-id="faf7c-111">De första tre kommandona konfigurera en offentlig IP-adress, en klient del och en avsökning för regel konfigurationen i det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="faf7c-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="faf7c-112">Med kommandot tillbaka skapas en ny regel som heter MyLBrule med vissa specifikationer.</span><span class="sxs-lookup"><span data-stu-id="faf7c-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="faf7c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="faf7c-113">PARAMETERS</span></span>

### <span data-ttu-id="faf7c-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="faf7c-114">-BackendAddressPool</span></span>
<span data-ttu-id="faf7c-115">Anger ett **BackendAddressPool** -objekt som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="faf7c-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="faf7c-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="faf7c-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="faf7c-117">Anger ID för ett **BackendAddressPool** -objekt som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="faf7c-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="faf7c-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="faf7c-118">-BackendPort</span></span>
<span data-ttu-id="faf7c-119">Anger Server dels porten för trafik som matchas av denna regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="faf7c-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="faf7c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf7c-120">-DefaultProfile</span></span>
<span data-ttu-id="faf7c-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="faf7c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faf7c-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="faf7c-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="faf7c-123">Konfigurerar SNAT för de virtuella datorerna i backend-poolen till att använda den publicIP-adress som anges i klient delen av regeln för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="faf7c-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="faf7c-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="faf7c-124">-EnableFloatingIP</span></span>
<span data-ttu-id="faf7c-125">Anger att denna cmdlet aktiverar en flytande IP-adress för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="faf7c-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="faf7c-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="faf7c-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="faf7c-127">Anger en lista över de front-IP-adresser som är associerade med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="faf7c-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="faf7c-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="faf7c-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="faf7c-129">Anger ID för en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="faf7c-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="faf7c-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="faf7c-130">-FrontendPort</span></span>
<span data-ttu-id="faf7c-131">Anger front porten som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="faf7c-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="faf7c-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="faf7c-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="faf7c-133">Anger hur lång tid, i minuter, som status för konversationer ska behållas i en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="faf7c-133">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="faf7c-134">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="faf7c-134">-LoadDistribution</span></span>
<span data-ttu-id="faf7c-135">Anger en belastnings fördelning.</span><span class="sxs-lookup"><span data-stu-id="faf7c-135">Specifies a load distribution.</span></span>
<span data-ttu-id="faf7c-136">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="faf7c-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="faf7c-137">Vis</span><span class="sxs-lookup"><span data-stu-id="faf7c-137">Default</span></span>
- <span data-ttu-id="faf7c-138">SourceIP</span><span class="sxs-lookup"><span data-stu-id="faf7c-138">SourceIP</span></span>
- <span data-ttu-id="faf7c-139">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="faf7c-139">SourceIPProtocol</span></span>

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

### <span data-ttu-id="faf7c-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="faf7c-140">-Name</span></span>
<span data-ttu-id="faf7c-141">Anger namnet på den regler för belastnings utjämning som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="faf7c-141">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="faf7c-142">-Sond</span><span class="sxs-lookup"><span data-stu-id="faf7c-142">-Probe</span></span>
<span data-ttu-id="faf7c-143">Anger en sond som associeras med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="faf7c-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="faf7c-144">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="faf7c-144">-ProbeId</span></span>
<span data-ttu-id="faf7c-145">Anger ID för den sond som ska kopplas till en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="faf7c-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="faf7c-146">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="faf7c-146">-Protocol</span></span>
<span data-ttu-id="faf7c-147">Anger det protokoll som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="faf7c-147">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="faf7c-148">De acceptabla värdena för denna parameter är: TCP eller UDP.</span><span class="sxs-lookup"><span data-stu-id="faf7c-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="faf7c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf7c-149">CommonParameters</span></span>
<span data-ttu-id="faf7c-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faf7c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf7c-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faf7c-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf7c-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="faf7c-152">INPUTS</span></span>

### <span data-ttu-id="faf7c-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="faf7c-153">None</span></span>
<span data-ttu-id="faf7c-154">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="faf7c-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="faf7c-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="faf7c-155">OUTPUTS</span></span>

### <span data-ttu-id="faf7c-156">Microsoft. Azure. commands. Networks. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="faf7c-156">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="faf7c-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="faf7c-157">NOTES</span></span>

## <span data-ttu-id="faf7c-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="faf7c-158">RELATED LINKS</span></span>

[<span data-ttu-id="faf7c-159">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="faf7c-159">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="faf7c-160">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="faf7c-160">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="faf7c-161">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="faf7c-161">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="faf7c-162">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="faf7c-162">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


