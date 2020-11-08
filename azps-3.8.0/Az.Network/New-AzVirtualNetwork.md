---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: 9858355ded7e5105c1728561b73b6fa9e6c8a199
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090960"
---
# <span data-ttu-id="37bf6-101">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="37bf6-101">New-AzVirtualNetwork</span></span>

## <span data-ttu-id="37bf6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="37bf6-103">Skapar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="37bf6-103">Creates a virtual network.</span></span>

## <span data-ttu-id="37bf6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37bf6-104">SYNTAX</span></span>

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String> -AddressPrefix <String[]>
 [-DnsServer <String[]>] [-Subnet <PSSubnet[]>] [-BgpCommunity <String>] [-Tag <Hashtable>]
 [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37bf6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37bf6-105">DESCRIPTION</span></span>
<span data-ttu-id="37bf6-106">Cmdleten **New-AzVirtualNetwork** skapar ett Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="37bf6-106">The **New-AzVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="37bf6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37bf6-107">EXAMPLES</span></span>

### <span data-ttu-id="37bf6-108">1: skapa ett virtuellt nätverk med två undernät</span><span class="sxs-lookup"><span data-stu-id="37bf6-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="37bf6-109">I det här exemplet skapas ett virtuellt nätverk med två undernät.</span><span class="sxs-lookup"><span data-stu-id="37bf6-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="37bf6-110">Först skapas en ny resurs grupp i det centrala området.</span><span class="sxs-lookup"><span data-stu-id="37bf6-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="37bf6-111">Sedan skapar exemplet i minnet representationer av två undernät.</span><span class="sxs-lookup"><span data-stu-id="37bf6-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="37bf6-112">New-AzVirtualNetworkSubnetConfig cmdlet skapar inte något undernät på Server sidan.</span><span class="sxs-lookup"><span data-stu-id="37bf6-112">The New-AzVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="37bf6-113">Det finns ett undernät med namnet frontendSubnet och ett undernät som heter backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="37bf6-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="37bf6-114">New-AzVirtualNetwork-cmdleten skapar då ett virtuellt nätverk med hjälp av CIDR 10.0.0.0/16 som adressprefix och två undernät.</span><span class="sxs-lookup"><span data-stu-id="37bf6-114">The New-AzVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="37bf6-115">2: skapa ett virtuellt nätverk med DNS-inställningar</span><span class="sxs-lookup"><span data-stu-id="37bf6-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="37bf6-116">I det här exemplet skapas ett virtuellt nätverk med två undernät och två DNS-servrar.</span><span class="sxs-lookup"><span data-stu-id="37bf6-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="37bf6-117">Effekten av att ange DNS-servrarna i det virtuella nätverket är att de nätverkskort som distribueras till detta virtuella nätverk ärver dessa DNS-servrar som standard.</span><span class="sxs-lookup"><span data-stu-id="37bf6-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="37bf6-118">Dessa standarder kan skrivas över per nätverkskort via en inställning på NÄTVERKSKORTet.</span><span class="sxs-lookup"><span data-stu-id="37bf6-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="37bf6-119">Om inga DNS-servrar anges i ett VNET och inga DNS-servrar på nätverkskorten används standard-DNS-servrarna för DNS-matchning.</span><span class="sxs-lookup"><span data-stu-id="37bf6-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="37bf6-120">3: skapa ett virtuellt nätverk med ett undernät som hänvisar till en nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="37bf6-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="37bf6-121">I det här exemplet skapas ett virtuellt nätverk med undernät som hänvisar till en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="37bf6-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="37bf6-122">Först skapar exemplet en resurs grupp som en behållare för de resurser som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="37bf6-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="37bf6-123">Därefter skapas en nätverks säkerhets grupp som tillåter inkommande RDP-åtkomst, men på annat sätt tvingas standard reglerna för nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="37bf6-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="37bf6-124">New-AzVirtualNetworkSubnetConfig-cmdleten skapar sedan en minnes presentation i två undernät som båda hänvisar till nätverks säkerhets gruppen som skapades.</span><span class="sxs-lookup"><span data-stu-id="37bf6-124">The New-AzVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="37bf6-125">Kommandot New-AzVirtualNetwork skapar sedan det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="37bf6-125">The New-AzVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="37bf6-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37bf6-126">PARAMETERS</span></span>

### <span data-ttu-id="37bf6-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="37bf6-127">-AddressPrefix</span></span>
<span data-ttu-id="37bf6-128">Anger ett intervall med IP-adresser för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="37bf6-128">Specifies a range of IP addresses for a virtual network.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37bf6-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37bf6-129">-AsJob</span></span>
<span data-ttu-id="37bf6-130">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="37bf6-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37bf6-131">-BgpCommunity</span><span class="sxs-lookup"><span data-stu-id="37bf6-131">-BgpCommunity</span></span>
<span data-ttu-id="37bf6-132">BGP-communityn annonserades via ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="37bf6-132">The BGP Community advertised over ExpressRoute.</span></span>

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

### <span data-ttu-id="37bf6-133">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="37bf6-133">-DdosProtectionPlanId</span></span>
<span data-ttu-id="37bf6-134">Referens till den DDoS skydds plan resursen som är associerad med det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="37bf6-134">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

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

### <span data-ttu-id="37bf6-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37bf6-135">-DefaultProfile</span></span>
<span data-ttu-id="37bf6-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="37bf6-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37bf6-137">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="37bf6-137">-DnsServer</span></span>
<span data-ttu-id="37bf6-138">Anger DNS-server för ett undernät.</span><span class="sxs-lookup"><span data-stu-id="37bf6-138">Specifies the DNS server for a subnet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37bf6-139">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="37bf6-139">-EnableDdosProtection</span></span>
<span data-ttu-id="37bf6-140">En växel parameter som representerar om DDoS skydd är aktiverat eller inte.</span><span class="sxs-lookup"><span data-stu-id="37bf6-140">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bf6-141">-Force</span><span class="sxs-lookup"><span data-stu-id="37bf6-141">-Force</span></span>
<span data-ttu-id="37bf6-142">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="37bf6-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="37bf6-143">-Plats</span><span class="sxs-lookup"><span data-stu-id="37bf6-143">-Location</span></span>
<span data-ttu-id="37bf6-144">Anger regionen för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="37bf6-144">Specifies the region for the virtual network.</span></span>

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

### <span data-ttu-id="37bf6-145">-Namn</span><span class="sxs-lookup"><span data-stu-id="37bf6-145">-Name</span></span>
<span data-ttu-id="37bf6-146">Anger namnet på det virtuella nätverk som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="37bf6-146">Specifies the name of the virtual network that this cmdlet creates.</span></span>

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

### <span data-ttu-id="37bf6-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37bf6-147">-ResourceGroupName</span></span>
<span data-ttu-id="37bf6-148">Anger namnet på en resurs grupp som ska innehålla det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="37bf6-148">Specifies the name of a resource group to contain the virtual network.</span></span>

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

### <span data-ttu-id="37bf6-149">-Undernät</span><span class="sxs-lookup"><span data-stu-id="37bf6-149">-Subnet</span></span>
<span data-ttu-id="37bf6-150">Anger en lista över undernät som ska kopplas till det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="37bf6-150">Specifies a list of subnets to associate with the virtual network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37bf6-151">-Tagg</span><span class="sxs-lookup"><span data-stu-id="37bf6-151">-Tag</span></span>
<span data-ttu-id="37bf6-152">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="37bf6-152">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="37bf6-153">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="37bf6-153">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="37bf6-154">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="37bf6-154">-Confirm</span></span>
<span data-ttu-id="37bf6-155">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="37bf6-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37bf6-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37bf6-156">-WhatIf</span></span>
<span data-ttu-id="37bf6-157">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="37bf6-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37bf6-158">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="37bf6-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37bf6-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37bf6-159">CommonParameters</span></span>
<span data-ttu-id="37bf6-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37bf6-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37bf6-161">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37bf6-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37bf6-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37bf6-162">INPUTS</span></span>

### <span data-ttu-id="37bf6-163">System. String</span><span class="sxs-lookup"><span data-stu-id="37bf6-163">System.String</span></span>

### <span data-ttu-id="37bf6-164">System. string []</span><span class="sxs-lookup"><span data-stu-id="37bf6-164">System.String[]</span></span>

### <span data-ttu-id="37bf6-165">Microsoft. Azure. commands. Network. Models. PSSubnet []</span><span class="sxs-lookup"><span data-stu-id="37bf6-165">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span></span>

### <span data-ttu-id="37bf6-166">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="37bf6-166">System.Collections.Hashtable</span></span>

## <span data-ttu-id="37bf6-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37bf6-167">OUTPUTS</span></span>

### <span data-ttu-id="37bf6-168">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="37bf6-168">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="37bf6-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37bf6-169">NOTES</span></span>

## <span data-ttu-id="37bf6-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37bf6-170">RELATED LINKS</span></span>

[<span data-ttu-id="37bf6-171">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="37bf6-171">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="37bf6-172">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="37bf6-172">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="37bf6-173">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="37bf6-173">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="37bf6-174">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="37bf6-174">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)
