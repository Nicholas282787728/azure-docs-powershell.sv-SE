---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: a81f8b260b0631692bb24a571bcb86b8ecf038d3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930950"
---
# <span data-ttu-id="c062a-101">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c062a-101">New-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="c062a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c062a-102">SYNOPSIS</span></span>
<span data-ttu-id="c062a-103">Skapar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="c062a-103">Creates a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c062a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c062a-104">SYNTAX</span></span>

```
New-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-Subnet <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]>]
 [-Tag <Hashtable>] [-EnableDDoSProtection] [-EnableVmProtection] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c062a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c062a-105">DESCRIPTION</span></span>
<span data-ttu-id="c062a-106">Cmdleten **New-AzureRmVirtualNetwork** skapar ett Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="c062a-106">The **New-AzureRmVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="c062a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c062a-107">EXAMPLES</span></span>

### <span data-ttu-id="c062a-108">1: skapa ett virtuellt nätverk med två undernät</span><span class="sxs-lookup"><span data-stu-id="c062a-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="c062a-109">I det här exemplet skapas ett virtuellt nätverk med två undernät.</span><span class="sxs-lookup"><span data-stu-id="c062a-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="c062a-110">Först skapas en ny resurs grupp i det centrala området.</span><span class="sxs-lookup"><span data-stu-id="c062a-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="c062a-111">Sedan skapar exemplet i minnet representationer av två undernät.</span><span class="sxs-lookup"><span data-stu-id="c062a-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="c062a-112">New-AzureRmVirtualNetworkSubnetConfig cmdlet skapar inte något undernät på Server sidan.</span><span class="sxs-lookup"><span data-stu-id="c062a-112">The New-AzureRmVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="c062a-113">Det finns ett undernät med namnet frontendSubnet och ett undernät som heter backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="c062a-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="c062a-114">New-AzureRmVirtualNetwork-cmdleten skapar då ett virtuellt nätverk med hjälp av CIDR 10.0.0.0/16 som adressprefix och två undernät.</span><span class="sxs-lookup"><span data-stu-id="c062a-114">The New-AzureRmVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="c062a-115">2: skapa ett virtuellt nätverk med DNS-inställningar</span><span class="sxs-lookup"><span data-stu-id="c062a-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="c062a-116">I det här exemplet skapas ett virtuellt nätverk med två undernät och två DNS-servrar.</span><span class="sxs-lookup"><span data-stu-id="c062a-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="c062a-117">Effekten av att ange DNS-servrarna i det virtuella nätverket är att de nätverkskort som distribueras till detta virtuella nätverk ärver dessa DNS-servrar som standard.</span><span class="sxs-lookup"><span data-stu-id="c062a-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="c062a-118">Dessa standarder kan skrivas över per nätverkskort via en inställning på NÄTVERKSKORTet.</span><span class="sxs-lookup"><span data-stu-id="c062a-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="c062a-119">Om inga DNS-servrar anges i ett VNET och inga DNS-servrar på nätverkskorten används standard-DNS-servrarna för DNS-matchning.</span><span class="sxs-lookup"><span data-stu-id="c062a-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="c062a-120">3: skapa ett virtuellt nätverk med ett undernät som hänvisar till en nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="c062a-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="c062a-121">I det här exemplet skapas ett virtuellt nätverk med undernät som hänvisar till en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="c062a-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="c062a-122">Först skapar exemplet en resurs grupp som en behållare för de resurser som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="c062a-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="c062a-123">Därefter skapas en nätverks säkerhets grupp som tillåter inkommande RDP-åtkomst, men på annat sätt tvingas standard reglerna för nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="c062a-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="c062a-124">New-AzureRmVirtualNetworkSubnetConfig-cmdleten skapar sedan en minnes presentation i två undernät som båda hänvisar till nätverks säkerhets gruppen som skapades.</span><span class="sxs-lookup"><span data-stu-id="c062a-124">The New-AzureRmVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="c062a-125">Kommandot New-AzureRmVirtualNetwork skapar sedan det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="c062a-125">The New-AzureRmVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="c062a-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c062a-126">PARAMETERS</span></span>

### <span data-ttu-id="c062a-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c062a-127">-AddressPrefix</span></span>
<span data-ttu-id="c062a-128">Anger ett intervall med IP-adresser för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="c062a-128">Specifies a range of IP addresses for a virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c062a-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c062a-129">-AsJob</span></span>
<span data-ttu-id="c062a-130">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c062a-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c062a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c062a-131">-DefaultProfile</span></span>
<span data-ttu-id="c062a-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c062a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c062a-133">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="c062a-133">-DnsServer</span></span>
<span data-ttu-id="c062a-134">Anger DNS-server för ett undernät.</span><span class="sxs-lookup"><span data-stu-id="c062a-134">Specifies the DNS server for a subnet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c062a-135">-EnableDDoSProtection</span><span class="sxs-lookup"><span data-stu-id="c062a-135">-EnableDDoSProtection</span></span>
<span data-ttu-id="c062a-136">En växel parameter som representerar om DDoS skydd är aktiverat eller inte.</span><span class="sxs-lookup"><span data-stu-id="c062a-136">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c062a-137">-EnableVmProtection</span><span class="sxs-lookup"><span data-stu-id="c062a-137">-EnableVmProtection</span></span>
<span data-ttu-id="c062a-138">En växel parameter som representerar om VM-skyddet är aktiverat eller inte.</span><span class="sxs-lookup"><span data-stu-id="c062a-138">A switch parameter which represents if Vm protection is enabled or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c062a-139">-Force</span><span class="sxs-lookup"><span data-stu-id="c062a-139">-Force</span></span>
<span data-ttu-id="c062a-140">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c062a-140">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c062a-141">-Plats</span><span class="sxs-lookup"><span data-stu-id="c062a-141">-Location</span></span>
<span data-ttu-id="c062a-142">Anger regionen för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="c062a-142">Specifies the region for the virtual network.</span></span>

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

### <span data-ttu-id="c062a-143">-Namn</span><span class="sxs-lookup"><span data-stu-id="c062a-143">-Name</span></span>
<span data-ttu-id="c062a-144">Anger namnet på det virtuella nätverk som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="c062a-144">Specifies the name of the virtual network that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c062a-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c062a-145">-ResourceGroupName</span></span>
<span data-ttu-id="c062a-146">Anger namnet på en resurs grupp som ska innehålla det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="c062a-146">Specifies the name of a resource group to contain the virtual network.</span></span>

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

### <span data-ttu-id="c062a-147">-Undernät</span><span class="sxs-lookup"><span data-stu-id="c062a-147">-Subnet</span></span>
<span data-ttu-id="c062a-148">Anger en lista över undernät som ska kopplas till det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="c062a-148">Specifies a list of subnets to associate with the virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c062a-149">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c062a-149">-Tag</span></span>
<span data-ttu-id="c062a-150">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c062a-150">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c062a-151">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="c062a-151">For example:</span></span>

<span data-ttu-id="c062a-152">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="c062a-152">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c062a-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c062a-153">-Confirm</span></span>
<span data-ttu-id="c062a-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c062a-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c062a-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c062a-155">-WhatIf</span></span>
<span data-ttu-id="c062a-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c062a-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c062a-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c062a-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c062a-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c062a-158">CommonParameters</span></span>
<span data-ttu-id="c062a-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c062a-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c062a-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c062a-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c062a-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c062a-161">INPUTS</span></span>

## <span data-ttu-id="c062a-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c062a-162">OUTPUTS</span></span>

### <span data-ttu-id="c062a-163">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c062a-163">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="c062a-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c062a-164">NOTES</span></span>

## <span data-ttu-id="c062a-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c062a-165">RELATED LINKS</span></span>

[<span data-ttu-id="c062a-166">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c062a-166">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="c062a-167">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c062a-167">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="c062a-168">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c062a-168">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)
