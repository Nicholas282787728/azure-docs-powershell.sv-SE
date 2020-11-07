---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: 0b839d0392153fc21b9d57c15a823158827bdc72
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747990"
---
# <span data-ttu-id="4f249-101">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4f249-101">New-AzVirtualNetwork</span></span>

## <span data-ttu-id="4f249-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f249-102">SYNOPSIS</span></span>
<span data-ttu-id="4f249-103">Skapar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="4f249-103">Creates a virtual network.</span></span>

## <span data-ttu-id="4f249-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f249-104">SYNTAX</span></span>

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String> -AddressPrefix <String[]>
 [-DnsServer <String[]>] [-Subnet <PSSubnet[]>] [-Tag <Hashtable>] [-EnableDdosProtection]
 [-DdosProtectionPlanId <String>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f249-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f249-105">DESCRIPTION</span></span>
<span data-ttu-id="4f249-106">Cmdleten **New-AzVirtualNetwork** skapar ett Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="4f249-106">The **New-AzVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="4f249-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f249-107">EXAMPLES</span></span>

### <span data-ttu-id="4f249-108">1: skapa ett virtuellt nätverk med två undernät</span><span class="sxs-lookup"><span data-stu-id="4f249-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="4f249-109">I det här exemplet skapas ett virtuellt nätverk med två undernät.</span><span class="sxs-lookup"><span data-stu-id="4f249-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="4f249-110">Först skapas en ny resurs grupp i det centrala området.</span><span class="sxs-lookup"><span data-stu-id="4f249-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="4f249-111">Sedan skapar exemplet i minnet representationer av två undernät.</span><span class="sxs-lookup"><span data-stu-id="4f249-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="4f249-112">New-AzVirtualNetworkSubnetConfig cmdlet skapar inte något undernät på Server sidan.</span><span class="sxs-lookup"><span data-stu-id="4f249-112">The New-AzVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="4f249-113">Det finns ett undernät med namnet frontendSubnet och ett undernät som heter backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="4f249-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="4f249-114">New-AzVirtualNetwork-cmdleten skapar då ett virtuellt nätverk med hjälp av CIDR 10.0.0.0/16 som adressprefix och två undernät.</span><span class="sxs-lookup"><span data-stu-id="4f249-114">The New-AzVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="4f249-115">2: skapa ett virtuellt nätverk med DNS-inställningar</span><span class="sxs-lookup"><span data-stu-id="4f249-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="4f249-116">I det här exemplet skapas ett virtuellt nätverk med två undernät och två DNS-servrar.</span><span class="sxs-lookup"><span data-stu-id="4f249-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="4f249-117">Effekten av att ange DNS-servrarna i det virtuella nätverket är att de nätverkskort som distribueras till detta virtuella nätverk ärver dessa DNS-servrar som standard.</span><span class="sxs-lookup"><span data-stu-id="4f249-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="4f249-118">Dessa standarder kan skrivas över per nätverkskort via en inställning på NÄTVERKSKORTet.</span><span class="sxs-lookup"><span data-stu-id="4f249-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="4f249-119">Om inga DNS-servrar anges i ett VNET och inga DNS-servrar på nätverkskorten används standard-DNS-servrarna för DNS-matchning.</span><span class="sxs-lookup"><span data-stu-id="4f249-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="4f249-120">3: skapa ett virtuellt nätverk med ett undernät som hänvisar till en nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="4f249-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="4f249-121">I det här exemplet skapas ett virtuellt nätverk med undernät som hänvisar till en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="4f249-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="4f249-122">Först skapar exemplet en resurs grupp som en behållare för de resurser som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="4f249-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="4f249-123">Därefter skapas en nätverks säkerhets grupp som tillåter inkommande RDP-åtkomst, men på annat sätt tvingas standard reglerna för nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="4f249-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="4f249-124">New-AzVirtualNetworkSubnetConfig-cmdleten skapar sedan en minnes presentation i två undernät som båda hänvisar till nätverks säkerhets gruppen som skapades.</span><span class="sxs-lookup"><span data-stu-id="4f249-124">The New-AzVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="4f249-125">Kommandot New-AzVirtualNetwork skapar sedan det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="4f249-125">The New-AzVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="4f249-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f249-126">PARAMETERS</span></span>

### <span data-ttu-id="4f249-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4f249-127">-AddressPrefix</span></span>
<span data-ttu-id="4f249-128">Anger ett intervall med IP-adresser för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="4f249-128">Specifies a range of IP addresses for a virtual network.</span></span>

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

### <span data-ttu-id="4f249-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f249-129">-AsJob</span></span>
<span data-ttu-id="4f249-130">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4f249-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f249-131">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="4f249-131">-DdosProtectionPlanId</span></span>
<span data-ttu-id="4f249-132">Referens till den DDoS skydds plan resursen som är associerad med det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="4f249-132">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

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

### <span data-ttu-id="4f249-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f249-133">-DefaultProfile</span></span>
<span data-ttu-id="4f249-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f249-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f249-135">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="4f249-135">-DnsServer</span></span>
<span data-ttu-id="4f249-136">Anger DNS-server för ett undernät.</span><span class="sxs-lookup"><span data-stu-id="4f249-136">Specifies the DNS server for a subnet.</span></span>

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

### <span data-ttu-id="4f249-137">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="4f249-137">-EnableDdosProtection</span></span>
<span data-ttu-id="4f249-138">En växel parameter som representerar om DDoS skydd är aktiverat eller inte.</span><span class="sxs-lookup"><span data-stu-id="4f249-138">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

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

### <span data-ttu-id="4f249-139">-Force</span><span class="sxs-lookup"><span data-stu-id="4f249-139">-Force</span></span>
<span data-ttu-id="4f249-140">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4f249-140">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4f249-141">-Plats</span><span class="sxs-lookup"><span data-stu-id="4f249-141">-Location</span></span>
<span data-ttu-id="4f249-142">Anger regionen för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="4f249-142">Specifies the region for the virtual network.</span></span>

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

### <span data-ttu-id="4f249-143">-Namn</span><span class="sxs-lookup"><span data-stu-id="4f249-143">-Name</span></span>
<span data-ttu-id="4f249-144">Anger namnet på det virtuella nätverk som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="4f249-144">Specifies the name of the virtual network that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4f249-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f249-145">-ResourceGroupName</span></span>
<span data-ttu-id="4f249-146">Anger namnet på en resurs grupp som ska innehålla det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="4f249-146">Specifies the name of a resource group to contain the virtual network.</span></span>

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

### <span data-ttu-id="4f249-147">-Undernät</span><span class="sxs-lookup"><span data-stu-id="4f249-147">-Subnet</span></span>
<span data-ttu-id="4f249-148">Anger en lista över undernät som ska kopplas till det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="4f249-148">Specifies a list of subnets to associate with the virtual network.</span></span>

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

### <span data-ttu-id="4f249-149">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4f249-149">-Tag</span></span>
<span data-ttu-id="4f249-150">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4f249-150">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4f249-151">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="4f249-151">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4f249-152">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4f249-152">-Confirm</span></span>
<span data-ttu-id="4f249-153">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4f249-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f249-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f249-154">-WhatIf</span></span>
<span data-ttu-id="4f249-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4f249-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f249-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4f249-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f249-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f249-157">CommonParameters</span></span>
<span data-ttu-id="4f249-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f249-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f249-159">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f249-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f249-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f249-160">INPUTS</span></span>

### <span data-ttu-id="4f249-161">System. String</span><span class="sxs-lookup"><span data-stu-id="4f249-161">System.String</span></span>

### <span data-ttu-id="4f249-162">System. string []</span><span class="sxs-lookup"><span data-stu-id="4f249-162">System.String[]</span></span>

### <span data-ttu-id="4f249-163">Microsoft. Azure. commands. Network. Models. PSSubnet []</span><span class="sxs-lookup"><span data-stu-id="4f249-163">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span></span>

### <span data-ttu-id="4f249-164">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="4f249-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4f249-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f249-165">OUTPUTS</span></span>

### <span data-ttu-id="4f249-166">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4f249-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="4f249-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f249-167">NOTES</span></span>

## <span data-ttu-id="4f249-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f249-168">RELATED LINKS</span></span>

[<span data-ttu-id="4f249-169">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4f249-169">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="4f249-170">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4f249-170">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="4f249-171">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4f249-171">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="4f249-172">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="4f249-172">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)
