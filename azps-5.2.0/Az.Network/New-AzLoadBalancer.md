---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: 558f7bb9937d52117f37cc4964d4dc925b0dca47
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407339"
---
# <span data-ttu-id="661a3-101">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="661a3-101">New-AzLoadBalancer</span></span>

## <span data-ttu-id="661a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="661a3-102">SYNOPSIS</span></span>
<span data-ttu-id="661a3-103">Skapar en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="661a3-103">Creates a load balancer.</span></span>

## <span data-ttu-id="661a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="661a3-104">SYNTAX</span></span>

```
New-AzLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>] [-Tier <String>] [-FrontendIpConfiguration <PSFrontendIPConfiguration[]>]
 [-BackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancingRule <PSLoadBalancingRule[]>]
 [-Probe <PSProbe[]>] [-InboundNatRule <PSInboundNatRule[]>] [-InboundNatPool <PSInboundNatPool[]>]
 [-OutboundRule <PSOutboundRule[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="661a3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="661a3-105">DESCRIPTION</span></span>
<span data-ttu-id="661a3-106">Cmdleten **New-AzLoadBalancer** skapar en Azure belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="661a3-106">The **New-AzLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="661a3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="661a3-107">EXAMPLES</span></span>

### <span data-ttu-id="661a3-108">Exempel 1: skapa en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="661a3-108">Example 1: Create a load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="661a3-109">För att distribuera en belastningsutjämnare måste du först skapa flera objekt och de första sju kommandona visar hur du skapar objekten.</span><span class="sxs-lookup"><span data-stu-id="661a3-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="661a3-110">Med kommandot åtto skapas en belastningsutjämnare med namnet MyLoadBalancer i resurs gruppen med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="661a3-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="661a3-111">Det nionde och sista kommandot får den nya belastningsutjämnaren för att kontrol lera att den har skapats.</span><span class="sxs-lookup"><span data-stu-id="661a3-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="661a3-112">Observera att det här exemplet visar hur du skapar en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="661a3-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="661a3-113">Du måste också konfigurera den med hjälp av Add-AzNetworkInterfaceIpConfig cmdlet för att koppla nätverkskorten till olika virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="661a3-113">You must also configure it using the Add-AzNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

### <span data-ttu-id="661a3-114">Exempel 2: skapa en global belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="661a3-114">Example 2: Create a global load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -name "MyPublicIp" -Location "West US" -AllocationMethod Static -DomainNameLabel $domainNameLabel -Sku Standard -Tier Global
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig01"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP -DisableOutboundSNAT
PS C:\> lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -LoadBalancingRule $lbrule -Sku Standard -Tier Global        
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="661a3-115">För att distribuera en global belastningsutjämnare måste du först skapa flera objekt och de första fem kommandona visar hur du skapar objekten.</span><span class="sxs-lookup"><span data-stu-id="661a3-115">Deploying a global load balancer requires that you first create several objects, and the first five commands show how to create those objects.</span></span>
<span data-ttu-id="661a3-116">Med det sjätte kommandot skapar du belastningsutjämnaren med namnet MyLoadBalancer i resurs gruppen med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="661a3-116">The sixth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="661a3-117">Det sjunde och sista kommandot får den nya belastningsutjämnaren för att kontrol lera att den har skapats.</span><span class="sxs-lookup"><span data-stu-id="661a3-117">The seventh and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="661a3-118">Observera att det här exemplet visar hur du skapar en global belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="661a3-118">Note that this example only shows how to create a global load balancer.</span></span> <span data-ttu-id="661a3-119">Du måste också konfigurera den med hjälp av New-AzLoadBalancerBackendAddressConfig cmdlet för att tilldela regionala startpooler-ID: n till backend-adresspoolen</span><span class="sxs-lookup"><span data-stu-id="661a3-119">You must also configure it using the New-AzLoadBalancerBackendAddressConfig cmdlet to assign regional load balancer frontend ipconfig ids to its backend address pool</span></span>

## <span data-ttu-id="661a3-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="661a3-120">PARAMETERS</span></span>

### <span data-ttu-id="661a3-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="661a3-121">-AsJob</span></span>
<span data-ttu-id="661a3-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="661a3-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="661a3-123">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="661a3-123">-BackendAddressPool</span></span>
<span data-ttu-id="661a3-124">Anger en server dels adresspool att koppla till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="661a3-124">Specifies a backend address pool to associate with a load balancer.</span></span>

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

### <span data-ttu-id="661a3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="661a3-125">-DefaultProfile</span></span>
<span data-ttu-id="661a3-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="661a3-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="661a3-127">-Force</span><span class="sxs-lookup"><span data-stu-id="661a3-127">-Force</span></span>
<span data-ttu-id="661a3-128">Anger att denna cmdlet skapar en belastningsutjämnare även om det redan finns en belastningsutjämnare med samma namn.</span><span class="sxs-lookup"><span data-stu-id="661a3-128">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="661a3-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="661a3-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="661a3-130">Anger en lista över de front-IP-adresser som ska kopplas till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="661a3-130">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

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

### <span data-ttu-id="661a3-131">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="661a3-131">-InboundNatPool</span></span>
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

### <span data-ttu-id="661a3-132">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="661a3-132">-InboundNatRule</span></span>
<span data-ttu-id="661a3-133">Anger en lista över inkommande NAT-regler (Network Address Translation) som ska kopplas till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="661a3-133">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="661a3-134">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="661a3-134">-LoadBalancingRule</span></span>
<span data-ttu-id="661a3-135">Anger en lista över regler för belastnings utjämning som ska kopplas till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="661a3-135">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="661a3-136">-Plats</span><span class="sxs-lookup"><span data-stu-id="661a3-136">-Location</span></span>
<span data-ttu-id="661a3-137">Anger i vilken region du vill skapa en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="661a3-137">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="661a3-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="661a3-138">-Name</span></span>
<span data-ttu-id="661a3-139">Anger namnet på den belastningsutjämnare som skapas.</span><span class="sxs-lookup"><span data-stu-id="661a3-139">Specifies the name of the load balancer that this creates.</span></span>

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

### <span data-ttu-id="661a3-140">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="661a3-140">-OutboundRule</span></span>
<span data-ttu-id="661a3-141">Reglerna för utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="661a3-141">The outbound rules.</span></span>

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

### <span data-ttu-id="661a3-142">-Sond</span><span class="sxs-lookup"><span data-stu-id="661a3-142">-Probe</span></span>
<span data-ttu-id="661a3-143">Anger en lista över avsökningar som ska kopplas till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="661a3-143">Specifies a list of probes to associate with a load balancer.</span></span>

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

### <span data-ttu-id="661a3-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="661a3-144">-ResourceGroupName</span></span>
<span data-ttu-id="661a3-145">Anger namnet på den resurs grupp där belastningsutjämnaren ska skapas.</span><span class="sxs-lookup"><span data-stu-id="661a3-145">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="661a3-146">-SKU</span><span class="sxs-lookup"><span data-stu-id="661a3-146">-Sku</span></span>
<span data-ttu-id="661a3-147">SKU-namnet för belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="661a3-147">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="661a3-148">-Tagg</span><span class="sxs-lookup"><span data-stu-id="661a3-148">-Tag</span></span>
<span data-ttu-id="661a3-149">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="661a3-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="661a3-150">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="661a3-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="661a3-151">-Tier</span><span class="sxs-lookup"><span data-stu-id="661a3-151">-Tier</span></span>
<span data-ttu-id="661a3-152">SKU-nivån för belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="661a3-152">The load balancer Sku Tier.</span></span>

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

### <span data-ttu-id="661a3-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="661a3-153">-Confirm</span></span>
<span data-ttu-id="661a3-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="661a3-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="661a3-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="661a3-155">-WhatIf</span></span>
<span data-ttu-id="661a3-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="661a3-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="661a3-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="661a3-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="661a3-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="661a3-158">CommonParameters</span></span>
<span data-ttu-id="661a3-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="661a3-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="661a3-160">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="661a3-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="661a3-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="661a3-161">INPUTS</span></span>

### <span data-ttu-id="661a3-162">System. String</span><span class="sxs-lookup"><span data-stu-id="661a3-162">System.String</span></span>

### <span data-ttu-id="661a3-163">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="661a3-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="661a3-164">Microsoft. Azure. commands. Network. Models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="661a3-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="661a3-165">Microsoft. Azure. commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="661a3-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="661a3-166">Microsoft. Azure. commands. Network. Models. PSLoadBalancingRule []</span><span class="sxs-lookup"><span data-stu-id="661a3-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span></span>

### <span data-ttu-id="661a3-167">Microsoft. Azure. commands. Network. Models. PSProbe []</span><span class="sxs-lookup"><span data-stu-id="661a3-167">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span></span>

### <span data-ttu-id="661a3-168">Microsoft. Azure. commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="661a3-168">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="661a3-169">Microsoft. Azure. commands. Network. Models. PSInboundNatPool []</span><span class="sxs-lookup"><span data-stu-id="661a3-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span></span>

### <span data-ttu-id="661a3-170">Microsoft. Azure. commands. Network. Models. PSOutboundRule []</span><span class="sxs-lookup"><span data-stu-id="661a3-170">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span></span>

## <span data-ttu-id="661a3-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="661a3-171">OUTPUTS</span></span>

### <span data-ttu-id="661a3-172">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="661a3-172">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="661a3-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="661a3-173">NOTES</span></span>

## <span data-ttu-id="661a3-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="661a3-174">RELATED LINKS</span></span>

[<span data-ttu-id="661a3-175">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="661a3-175">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="661a3-176">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="661a3-176">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="661a3-177">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="661a3-177">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="661a3-178">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="661a3-178">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)
