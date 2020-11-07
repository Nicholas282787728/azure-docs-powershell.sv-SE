---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
ms.openlocfilehash: 9c52a5f234b374612b07d53b21ac9409a45cc35a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756377"
---
# <span data-ttu-id="133d2-101">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="133d2-101">New-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="133d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="133d2-102">SYNOPSIS</span></span>
<span data-ttu-id="133d2-103">Skapar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="133d2-103">Creates a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="133d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="133d2-104">SYNTAX</span></span>

```
New-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-Subnet <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]>]
 [-Tag <Hashtable>] [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-EnableVmProtection] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="133d2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="133d2-105">DESCRIPTION</span></span>
<span data-ttu-id="133d2-106">Cmdleten **New-AzureRmVirtualNetwork** skapar ett Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="133d2-106">The **New-AzureRmVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="133d2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="133d2-107">EXAMPLES</span></span>

### <span data-ttu-id="133d2-108">1: skapa ett virtuellt nätverk med två undernät</span><span class="sxs-lookup"><span data-stu-id="133d2-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="133d2-109">I det här exemplet skapas ett virtuellt nätverk med två undernät.</span><span class="sxs-lookup"><span data-stu-id="133d2-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="133d2-110">Först skapas en ny resurs grupp i det centrala området.</span><span class="sxs-lookup"><span data-stu-id="133d2-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="133d2-111">Sedan skapar exemplet i minnet representationer av två undernät.</span><span class="sxs-lookup"><span data-stu-id="133d2-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="133d2-112">New-AzureRmVirtualNetworkSubnetConfig cmdlet skapar inte något undernät på Server sidan.</span><span class="sxs-lookup"><span data-stu-id="133d2-112">The New-AzureRmVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="133d2-113">Det finns ett undernät med namnet frontendSubnet och ett undernät som heter backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="133d2-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="133d2-114">New-AzureRmVirtualNetwork-cmdleten skapar då ett virtuellt nätverk med hjälp av CIDR 10.0.0.0/16 som adressprefix och två undernät.</span><span class="sxs-lookup"><span data-stu-id="133d2-114">The New-AzureRmVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="133d2-115">2: skapa ett virtuellt nätverk med DNS-inställningar</span><span class="sxs-lookup"><span data-stu-id="133d2-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="133d2-116">I det här exemplet skapas ett virtuellt nätverk med två undernät och två DNS-servrar.</span><span class="sxs-lookup"><span data-stu-id="133d2-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="133d2-117">Effekten av att ange DNS-servrarna i det virtuella nätverket är att de nätverkskort som distribueras till detta virtuella nätverk ärver dessa DNS-servrar som standard.</span><span class="sxs-lookup"><span data-stu-id="133d2-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="133d2-118">Dessa standarder kan skrivas över per nätverkskort via en inställning på NÄTVERKSKORTet.</span><span class="sxs-lookup"><span data-stu-id="133d2-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="133d2-119">Om inga DNS-servrar anges i ett VNET och inga DNS-servrar på nätverkskorten används standard-DNS-servrarna för DNS-matchning.</span><span class="sxs-lookup"><span data-stu-id="133d2-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="133d2-120">3: skapa ett virtuellt nätverk med ett undernät som hänvisar till en nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="133d2-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="133d2-121">I det här exemplet skapas ett virtuellt nätverk med undernät som hänvisar till en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="133d2-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="133d2-122">Först skapar exemplet en resurs grupp som en behållare för de resurser som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="133d2-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="133d2-123">Därefter skapas en nätverks säkerhets grupp som tillåter inkommande RDP-åtkomst, men på annat sätt tvingas standard reglerna för nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="133d2-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="133d2-124">New-AzureRmVirtualNetworkSubnetConfig-cmdleten skapar sedan en minnes presentation i två undernät som båda hänvisar till nätverks säkerhets gruppen som skapades.</span><span class="sxs-lookup"><span data-stu-id="133d2-124">The New-AzureRmVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="133d2-125">Kommandot New-AzureRmVirtualNetwork skapar sedan det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="133d2-125">The New-AzureRmVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="133d2-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="133d2-126">PARAMETERS</span></span>

### <span data-ttu-id="133d2-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="133d2-127">-AddressPrefix</span></span>
<span data-ttu-id="133d2-128">Anger ett intervall med IP-adresser för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="133d2-128">Specifies a range of IP addresses for a virtual network.</span></span>

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

### <span data-ttu-id="133d2-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="133d2-129">-AsJob</span></span>
<span data-ttu-id="133d2-130">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="133d2-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="133d2-131">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="133d2-131">-DdosProtectionPlanId</span></span>
<span data-ttu-id="133d2-132">Referens till den DDoS skydds plan resursen som är associerad med det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="133d2-132">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

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

### <span data-ttu-id="133d2-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="133d2-133">-DefaultProfile</span></span>
<span data-ttu-id="133d2-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="133d2-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="133d2-135">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="133d2-135">-DnsServer</span></span>
<span data-ttu-id="133d2-136">Anger DNS-server för ett undernät.</span><span class="sxs-lookup"><span data-stu-id="133d2-136">Specifies the DNS server for a subnet.</span></span>

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

### <span data-ttu-id="133d2-137">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="133d2-137">-EnableDdosProtection</span></span>
<span data-ttu-id="133d2-138">En växel parameter som representerar om DDoS skydd är aktiverat eller inte.</span><span class="sxs-lookup"><span data-stu-id="133d2-138">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

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

### <span data-ttu-id="133d2-139">-EnableVmProtection</span><span class="sxs-lookup"><span data-stu-id="133d2-139">-EnableVmProtection</span></span>
<span data-ttu-id="133d2-140">En växel parameter som representerar om VM-skyddet är aktiverat eller inte.</span><span class="sxs-lookup"><span data-stu-id="133d2-140">A switch parameter which represents if Vm protection is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="133d2-141">-Force</span><span class="sxs-lookup"><span data-stu-id="133d2-141">-Force</span></span>
<span data-ttu-id="133d2-142">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="133d2-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="133d2-143">-Plats</span><span class="sxs-lookup"><span data-stu-id="133d2-143">-Location</span></span>
<span data-ttu-id="133d2-144">Anger regionen för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="133d2-144">Specifies the region for the virtual network.</span></span>

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

### <span data-ttu-id="133d2-145">-Namn</span><span class="sxs-lookup"><span data-stu-id="133d2-145">-Name</span></span>
<span data-ttu-id="133d2-146">Anger namnet på det virtuella nätverk som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="133d2-146">Specifies the name of the virtual network that this cmdlet creates.</span></span>

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

### <span data-ttu-id="133d2-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="133d2-147">-ResourceGroupName</span></span>
<span data-ttu-id="133d2-148">Anger namnet på en resurs grupp som ska innehålla det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="133d2-148">Specifies the name of a resource group to contain the virtual network.</span></span>

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

### <span data-ttu-id="133d2-149">-Undernät</span><span class="sxs-lookup"><span data-stu-id="133d2-149">-Subnet</span></span>
<span data-ttu-id="133d2-150">Anger en lista över undernät som ska kopplas till det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="133d2-150">Specifies a list of subnets to associate with the virtual network.</span></span>

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

### <span data-ttu-id="133d2-151">-Tagg</span><span class="sxs-lookup"><span data-stu-id="133d2-151">-Tag</span></span>
<span data-ttu-id="133d2-152">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="133d2-152">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="133d2-153">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="133d2-153">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="133d2-154">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="133d2-154">-Confirm</span></span>
<span data-ttu-id="133d2-155">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="133d2-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="133d2-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="133d2-156">-WhatIf</span></span>
<span data-ttu-id="133d2-157">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="133d2-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="133d2-158">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="133d2-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="133d2-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="133d2-159">CommonParameters</span></span>
<span data-ttu-id="133d2-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="133d2-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="133d2-161">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="133d2-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="133d2-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="133d2-162">INPUTS</span></span>

### <span data-ttu-id="133d2-163">System. String</span><span class="sxs-lookup"><span data-stu-id="133d2-163">System.String</span></span>

### <span data-ttu-id="133d2-164">System. Collections. Generic. list ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="133d2-164">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="133d2-165">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSSubnet, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="133d2-165">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSSubnet, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="133d2-166">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="133d2-166">System.Collections.Hashtable</span></span>

### <span data-ttu-id="133d2-167">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="133d2-167">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="133d2-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="133d2-168">OUTPUTS</span></span>

### <span data-ttu-id="133d2-169">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="133d2-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="133d2-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="133d2-170">NOTES</span></span>

## <span data-ttu-id="133d2-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="133d2-171">RELATED LINKS</span></span>

[<span data-ttu-id="133d2-172">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="133d2-172">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="133d2-173">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="133d2-173">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="133d2-174">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="133d2-174">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="133d2-175">New-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="133d2-175">New-AzureRmDdosProtectionPlan</span></span>](./New-AzureRmDdosProtectionPlan.md)
