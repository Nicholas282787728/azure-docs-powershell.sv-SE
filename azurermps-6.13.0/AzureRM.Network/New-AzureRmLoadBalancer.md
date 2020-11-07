---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancer.md
ms.openlocfilehash: db7d531b83dabe3bb5fc9dc79d86c3153d1553a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758159"
---
# <span data-ttu-id="a8822-101">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a8822-101">New-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="a8822-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8822-102">SYNOPSIS</span></span>
<span data-ttu-id="a8822-103">Skapar en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="a8822-103">Creates a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8822-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8822-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>]
 [-FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]>]
 [-BackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancingRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]>]
 [-Probe <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]>]
 [-InboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-InboundNatPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]>]
 [-OutboundRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSOutboundRule]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8822-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8822-105">DESCRIPTION</span></span>
<span data-ttu-id="a8822-106">Cmdleten **New-AzureRmLoadBalancer** skapar en Azure belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="a8822-106">The **New-AzureRmLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="a8822-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8822-107">EXAMPLES</span></span>

### <span data-ttu-id="a8822-108">Exempel 1: skapa en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="a8822-108">Example 1: Create a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a8822-109">För att distribuera en belastningsutjämnare måste du först skapa flera objekt och de första sju kommandona visar hur du skapar objekten.</span><span class="sxs-lookup"><span data-stu-id="a8822-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="a8822-110">Med kommandot åtto skapas en belastningsutjämnare med namnet MyLoadBalancer i resurs gruppen med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a8822-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="a8822-111">Det nionde och sista kommandot får den nya belastningsutjämnaren för att kontrol lera att den har skapats.</span><span class="sxs-lookup"><span data-stu-id="a8822-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="a8822-112">Observera att det här exemplet visar hur du skapar en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="a8822-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="a8822-113">Du måste också konfigurera den med hjälp av Add-AzureRmNetworkInterfaceIpConfig cmdlet för att koppla nätverkskorten till olika virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="a8822-113">You must also configure it using the Add-AzureRmNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="a8822-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8822-114">PARAMETERS</span></span>

### <span data-ttu-id="a8822-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8822-115">-AsJob</span></span>
<span data-ttu-id="a8822-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a8822-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8822-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a8822-117">-BackendAddressPool</span></span>
<span data-ttu-id="a8822-118">Anger en server dels adresspool att koppla till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="a8822-118">Specifies a backend address pool to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8822-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8822-119">-DefaultProfile</span></span>
<span data-ttu-id="a8822-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8822-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8822-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a8822-121">-Force</span></span>
<span data-ttu-id="a8822-122">Anger att denna cmdlet skapar en belastningsutjämnare även om det redan finns en belastningsutjämnare med samma namn.</span><span class="sxs-lookup"><span data-stu-id="a8822-122">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="a8822-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8822-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="a8822-124">Anger en lista över de front-IP-adresser som ska kopplas till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="a8822-124">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8822-125">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="a8822-125">-InboundNatPool</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8822-126">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="a8822-126">-InboundNatRule</span></span>
<span data-ttu-id="a8822-127">Anger en lista över inkommande NAT-regler (Network Address Translation) som ska kopplas till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="a8822-127">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8822-128">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="a8822-128">-LoadBalancingRule</span></span>
<span data-ttu-id="a8822-129">Anger en lista över regler för belastnings utjämning som ska kopplas till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="a8822-129">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8822-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="a8822-130">-Location</span></span>
<span data-ttu-id="a8822-131">Anger i vilken region du vill skapa en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="a8822-131">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="a8822-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="a8822-132">-Name</span></span>
<span data-ttu-id="a8822-133">Anger namnet på den belastningsutjämnare som skapas.</span><span class="sxs-lookup"><span data-stu-id="a8822-133">Specifies the name of the load balancer that this creates.</span></span>

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

### <span data-ttu-id="a8822-134">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="a8822-134">-OutboundRule</span></span>
<span data-ttu-id="a8822-135">Reglerna för utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="a8822-135">The outbound rules.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSOutboundRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8822-136">-Sond</span><span class="sxs-lookup"><span data-stu-id="a8822-136">-Probe</span></span>
<span data-ttu-id="a8822-137">Anger en lista över avsökningar som ska kopplas till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="a8822-137">Specifies a list of probes to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8822-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8822-138">-ResourceGroupName</span></span>
<span data-ttu-id="a8822-139">Anger namnet på den resurs grupp där belastningsutjämnaren ska skapas.</span><span class="sxs-lookup"><span data-stu-id="a8822-139">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="a8822-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="a8822-140">-Sku</span></span>
<span data-ttu-id="a8822-141">SKU-namnet för belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="a8822-141">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="a8822-142">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a8822-142">-Tag</span></span>
<span data-ttu-id="a8822-143">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a8822-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a8822-144">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="a8822-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a8822-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a8822-145">-Confirm</span></span>
<span data-ttu-id="a8822-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a8822-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8822-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8822-147">-WhatIf</span></span>
<span data-ttu-id="a8822-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a8822-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8822-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a8822-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8822-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8822-150">CommonParameters</span></span>
<span data-ttu-id="a8822-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8822-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8822-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8822-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8822-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8822-153">INPUTS</span></span>

### <span data-ttu-id="a8822-154">System. String</span><span class="sxs-lookup"><span data-stu-id="a8822-154">System.String</span></span>

### <span data-ttu-id="a8822-155">System. Collections. Generic. list \` 1 [[Microsoft. Azure. kommandon. Network. Models. PSFrontendIPConfiguration, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a8822-155">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a8822-156">System. Collections. Generic. list \` 1 [[Microsoft. Azure. kommandon. Network. Models. PSBackendAddressPool, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a8822-156">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a8822-157">System. Collections. Generic. list \` 1 [[Microsoft. Azure. kommandon. Network. Models. PSProbe, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a8822-157">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSProbe, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a8822-158">System. Collections. Generic. list \` 1 [[Microsoft. Azure. kommandon. Network. Models. PSInboundNatRule, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a8822-158">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a8822-159">System. Collections. Generic. list \` 1 [[Microsoft. Azure. kommandon. Network. Models. PSLoadBalancingRule, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a8822-159">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a8822-160">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="a8822-160">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a8822-161">System. Collections. Generic. list \` 1 [[Microsoft. Azure. kommandon. Network. Models. PSInboundNatPool, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a8822-161">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a8822-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8822-162">OUTPUTS</span></span>

### <span data-ttu-id="a8822-163">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a8822-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a8822-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8822-164">NOTES</span></span>

## <span data-ttu-id="a8822-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8822-165">RELATED LINKS</span></span>

[<span data-ttu-id="a8822-166">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a8822-166">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="a8822-167">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a8822-167">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="a8822-168">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a8822-168">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="a8822-169">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a8822-169">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)
