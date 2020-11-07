---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: fac34080ed9b96c30c9003cef57f73f416711ac5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922138"
---
# <span data-ttu-id="752b1-101">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="752b1-101">New-AzLoadBalancer</span></span>

## <span data-ttu-id="752b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="752b1-102">SYNOPSIS</span></span>
<span data-ttu-id="752b1-103">Skapar en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="752b1-103">Creates a load balancer.</span></span>

## <span data-ttu-id="752b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="752b1-104">SYNTAX</span></span>

```
New-AzLoadBalancer -Name <String> -ResourceGroupName <String> -Location <String> [-Sku <String>]
 [-FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]>]
 [-BackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-Probe <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]>]
 [-InboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-LoadBalancingRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]>]
 [-Tag <Hashtable>]
 [-InboundNatPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="752b1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="752b1-105">DESCRIPTION</span></span>
<span data-ttu-id="752b1-106">Cmdleten **New-AzLoadBalancer** skapar en Azure belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="752b1-106">The **New-AzLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="752b1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="752b1-107">EXAMPLES</span></span>

### <span data-ttu-id="752b1-108">Exempel 1: skapa en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="752b1-108">Example 1: Create a load balancer</span></span>
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

<span data-ttu-id="752b1-109">För att distribuera en belastningsutjämnare måste du först skapa flera objekt och de första sju kommandona visar hur du skapar objekten.</span><span class="sxs-lookup"><span data-stu-id="752b1-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>

<span data-ttu-id="752b1-110">Med kommandot åtto skapas en belastningsutjämnare med namnet MyLoadBalancer i resurs gruppen med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="752b1-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

<span data-ttu-id="752b1-111">Det nionde och sista kommandot får den nya belastningsutjämnaren för att kontrol lera att den har skapats.</span><span class="sxs-lookup"><span data-stu-id="752b1-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>

<span data-ttu-id="752b1-112">Observera att det här exemplet visar hur du skapar en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="752b1-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="752b1-113">Du måste också konfigurera den med hjälp av Add-AzNetworkInterfaceIpConfig cmdlet för att koppla nätverkskorten till olika virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="752b1-113">You must also configure it using the Add-AzNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="752b1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="752b1-114">PARAMETERS</span></span>

### <span data-ttu-id="752b1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="752b1-115">-AsJob</span></span>
<span data-ttu-id="752b1-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="752b1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="752b1-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="752b1-117">-BackendAddressPool</span></span>
<span data-ttu-id="752b1-118">Anger en server dels adresspool att koppla till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="752b1-118">Specifies a backend address pool to associate with a load balancer.</span></span>

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

### <span data-ttu-id="752b1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="752b1-119">-DefaultProfile</span></span>
<span data-ttu-id="752b1-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="752b1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="752b1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="752b1-121">-Force</span></span>
<span data-ttu-id="752b1-122">Anger att denna cmdlet skapar en belastningsutjämnare även om det redan finns en belastningsutjämnare med samma namn.</span><span class="sxs-lookup"><span data-stu-id="752b1-122">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="752b1-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="752b1-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="752b1-124">Anger en lista över de front-IP-adresser som ska kopplas till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="752b1-124">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

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

### <span data-ttu-id="752b1-125">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="752b1-125">-InboundNatPool</span></span>
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

### <span data-ttu-id="752b1-126">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="752b1-126">-InboundNatRule</span></span>
<span data-ttu-id="752b1-127">Anger en lista över inkommande NAT-regler (Network Address Translation) som ska kopplas till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="752b1-127">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="752b1-128">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="752b1-128">-LoadBalancingRule</span></span>
<span data-ttu-id="752b1-129">Anger en lista över regler för belastnings utjämning som ska kopplas till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="752b1-129">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="752b1-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="752b1-130">-Location</span></span>
<span data-ttu-id="752b1-131">Anger i vilken region du vill skapa en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="752b1-131">Specifies the region in which to create a load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="752b1-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="752b1-132">-Name</span></span>
<span data-ttu-id="752b1-133">Anger namnet på den belastningsutjämnare som skapas.</span><span class="sxs-lookup"><span data-stu-id="752b1-133">Specifies the name of the load balancer that this creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="752b1-134">-Sond</span><span class="sxs-lookup"><span data-stu-id="752b1-134">-Probe</span></span>
<span data-ttu-id="752b1-135">Anger en lista över avsökningar som ska kopplas till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="752b1-135">Specifies a list of probes to associate with a load balancer.</span></span>

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

### <span data-ttu-id="752b1-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="752b1-136">-ResourceGroupName</span></span>
<span data-ttu-id="752b1-137">Anger namnet på den resurs grupp där belastningsutjämnaren ska skapas.</span><span class="sxs-lookup"><span data-stu-id="752b1-137">Specifies the name of the resource group in which to create a load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="752b1-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="752b1-138">-Sku</span></span>
<span data-ttu-id="752b1-139">SKU-namnet för belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="752b1-139">The load balancer Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="752b1-140">-Tagg</span><span class="sxs-lookup"><span data-stu-id="752b1-140">-Tag</span></span>
<span data-ttu-id="752b1-141">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="752b1-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="752b1-142">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="752b1-142">For example:</span></span>

<span data-ttu-id="752b1-143">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="752b1-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="752b1-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="752b1-144">-Confirm</span></span>
<span data-ttu-id="752b1-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="752b1-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752b1-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="752b1-146">-WhatIf</span></span>
<span data-ttu-id="752b1-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="752b1-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="752b1-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="752b1-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752b1-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="752b1-149">CommonParameters</span></span>
<span data-ttu-id="752b1-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="752b1-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="752b1-151">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="752b1-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="752b1-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="752b1-152">INPUTS</span></span>

## <span data-ttu-id="752b1-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="752b1-153">OUTPUTS</span></span>

### <span data-ttu-id="752b1-154">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="752b1-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="752b1-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="752b1-155">NOTES</span></span>

## <span data-ttu-id="752b1-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="752b1-156">RELATED LINKS</span></span>

[<span data-ttu-id="752b1-157">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="752b1-157">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="752b1-158">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="752b1-158">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="752b1-159">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="752b1-159">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="752b1-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="752b1-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)
