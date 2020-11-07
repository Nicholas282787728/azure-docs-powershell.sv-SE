---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: 4e642f3aa93baad03a5b79a1736027353d5194bf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918273"
---
# <span data-ttu-id="f3e21-101">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f3e21-101">New-AzLoadBalancer</span></span>

## <span data-ttu-id="f3e21-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3e21-102">SYNOPSIS</span></span>
<span data-ttu-id="f3e21-103">Skapar en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="f3e21-103">Creates a load balancer.</span></span>

## <span data-ttu-id="f3e21-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3e21-104">SYNTAX</span></span>

```
New-AzLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>] [-FrontendIpConfiguration <PSFrontendIPConfiguration[]>]
 [-BackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancingRule <PSLoadBalancingRule[]>]
 [-Probe <PSProbe[]>] [-InboundNatRule <PSInboundNatRule[]>] [-InboundNatPool <PSInboundNatPool[]>]
 [-OutboundRule <PSOutboundRule[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3e21-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3e21-105">DESCRIPTION</span></span>
<span data-ttu-id="f3e21-106">Cmdleten **New-AzLoadBalancer** skapar en Azure belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="f3e21-106">The **New-AzLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="f3e21-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3e21-107">EXAMPLES</span></span>

### <span data-ttu-id="f3e21-108">Exempel 1: skapa en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="f3e21-108">Example 1: Create a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="f3e21-109">För att distribuera en belastningsutjämnare måste du först skapa flera objekt och de första sju kommandona visar hur du skapar objekten.</span><span class="sxs-lookup"><span data-stu-id="f3e21-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="f3e21-110">Med kommandot åtto skapas en belastningsutjämnare med namnet MyLoadBalancer i resurs gruppen med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f3e21-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="f3e21-111">Det nionde och sista kommandot får den nya belastningsutjämnaren för att kontrol lera att den har skapats.</span><span class="sxs-lookup"><span data-stu-id="f3e21-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="f3e21-112">Observera att det här exemplet visar hur du skapar en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="f3e21-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="f3e21-113">Du måste också konfigurera den med hjälp av Add-AzNetworkInterfaceIpConfig cmdlet för att koppla nätverkskorten till olika virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="f3e21-113">You must also configure it using the Add-AzNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="f3e21-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3e21-114">PARAMETERS</span></span>

### <span data-ttu-id="f3e21-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3e21-115">-AsJob</span></span>
<span data-ttu-id="f3e21-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f3e21-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3e21-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f3e21-117">-BackendAddressPool</span></span>
<span data-ttu-id="f3e21-118">Anger en server dels adresspool att koppla till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="f3e21-118">Specifies a backend address pool to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3e21-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3e21-119">-DefaultProfile</span></span>
<span data-ttu-id="f3e21-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f3e21-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3e21-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f3e21-121">-Force</span></span>
<span data-ttu-id="f3e21-122">Anger att denna cmdlet skapar en belastningsutjämnare även om det redan finns en belastningsutjämnare med samma namn.</span><span class="sxs-lookup"><span data-stu-id="f3e21-122">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="f3e21-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3e21-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="f3e21-124">Anger en lista över de front-IP-adresser som ska kopplas till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="f3e21-124">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3e21-125">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="f3e21-125">-InboundNatPool</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3e21-126">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="f3e21-126">-InboundNatRule</span></span>
<span data-ttu-id="f3e21-127">Anger en lista över inkommande NAT-regler (Network Address Translation) som ska kopplas till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="f3e21-127">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3e21-128">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="f3e21-128">-LoadBalancingRule</span></span>
<span data-ttu-id="f3e21-129">Anger en lista över regler för belastnings utjämning som ska kopplas till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="f3e21-129">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3e21-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="f3e21-130">-Location</span></span>
<span data-ttu-id="f3e21-131">Anger i vilken region du vill skapa en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="f3e21-131">Specifies the region in which to create a load balancer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3e21-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="f3e21-132">-Name</span></span>
<span data-ttu-id="f3e21-133">Anger namnet på den belastningsutjämnare som skapas.</span><span class="sxs-lookup"><span data-stu-id="f3e21-133">Specifies the name of the load balancer that this creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3e21-134">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="f3e21-134">-OutboundRule</span></span>
<span data-ttu-id="f3e21-135">Reglerna för utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="f3e21-135">The outbound rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3e21-136">-Sond</span><span class="sxs-lookup"><span data-stu-id="f3e21-136">-Probe</span></span>
<span data-ttu-id="f3e21-137">Anger en lista över avsökningar som ska kopplas till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="f3e21-137">Specifies a list of probes to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3e21-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3e21-138">-ResourceGroupName</span></span>
<span data-ttu-id="f3e21-139">Anger namnet på den resurs grupp där belastningsutjämnaren ska skapas.</span><span class="sxs-lookup"><span data-stu-id="f3e21-139">Specifies the name of the resource group in which to create a load balancer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3e21-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="f3e21-140">-Sku</span></span>
<span data-ttu-id="f3e21-141">SKU-namnet för belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="f3e21-141">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="f3e21-142">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f3e21-142">-Tag</span></span>
<span data-ttu-id="f3e21-143">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f3e21-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f3e21-144">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="f3e21-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3e21-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f3e21-145">-Confirm</span></span>
<span data-ttu-id="f3e21-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f3e21-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3e21-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3e21-147">-WhatIf</span></span>
<span data-ttu-id="f3e21-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f3e21-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3e21-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f3e21-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3e21-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3e21-150">CommonParameters</span></span>
<span data-ttu-id="f3e21-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3e21-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3e21-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3e21-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3e21-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3e21-153">INPUTS</span></span>

### <span data-ttu-id="f3e21-154">System. String</span><span class="sxs-lookup"><span data-stu-id="f3e21-154">System.String</span></span>

### <span data-ttu-id="f3e21-155">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="f3e21-155">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f3e21-156">Microsoft. Azure. commands. Network. Models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="f3e21-156">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="f3e21-157">Microsoft. Azure. commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="f3e21-157">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="f3e21-158">Microsoft. Azure. commands. Network. Models. PSLoadBalancingRule []</span><span class="sxs-lookup"><span data-stu-id="f3e21-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span></span>

### <span data-ttu-id="f3e21-159">Microsoft. Azure. commands. Network. Models. PSProbe []</span><span class="sxs-lookup"><span data-stu-id="f3e21-159">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span></span>

### <span data-ttu-id="f3e21-160">Microsoft. Azure. commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="f3e21-160">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="f3e21-161">Microsoft. Azure. commands. Network. Models. PSInboundNatPool []</span><span class="sxs-lookup"><span data-stu-id="f3e21-161">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span></span>

### <span data-ttu-id="f3e21-162">Microsoft. Azure. commands. Network. Models. PSOutboundRule []</span><span class="sxs-lookup"><span data-stu-id="f3e21-162">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span></span>

## <span data-ttu-id="f3e21-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3e21-163">OUTPUTS</span></span>

### <span data-ttu-id="f3e21-164">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f3e21-164">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f3e21-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3e21-165">NOTES</span></span>

## <span data-ttu-id="f3e21-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3e21-166">RELATED LINKS</span></span>

[<span data-ttu-id="f3e21-167">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f3e21-167">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f3e21-168">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f3e21-168">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f3e21-169">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f3e21-169">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="f3e21-170">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f3e21-170">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)
