---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 7596dff276a4913dd1c322ad023ebfb32b8e1aac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322506"
---
# <span data-ttu-id="f3c89-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f3c89-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="f3c89-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3c89-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c89-103">Lägger till en klient-IP-konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="f3c89-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="f3c89-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3c89-104">SYNTAX</span></span>

### <span data-ttu-id="f3c89-105">SetByResourceSubnet (standard)</span><span class="sxs-lookup"><span data-stu-id="f3c89-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3c89-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="f3c89-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3c89-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f3c89-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3c89-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f3c89-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3c89-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3c89-109">DESCRIPTION</span></span>
<span data-ttu-id="f3c89-110">Cmdleten **Add-AzLoadBalancerFrontendIpConfig** lägger till en klient-IP-konfiguration i en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="f3c89-110">The **Add-AzLoadBalancerFrontendIpConfig** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="f3c89-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3c89-111">EXAMPLES</span></span>

### <span data-ttu-id="f3c89-112">Exempel 1 lägga till en front-IP-konfiguration med en dynamisk IP-adress</span><span class="sxs-lookup"><span data-stu-id="f3c89-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="f3c89-113">Det första kommandot får det Azure Virtual Network som heter MyVnet och skickar resultatet med pipeline till cmdleten **Get-AzVirtualNetworkSubnetConfig** för att hämta under nätet med namnet mina undernät.</span><span class="sxs-lookup"><span data-stu-id="f3c89-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="f3c89-114">Då sparas resultatet i variabeln $Subnet.</span><span class="sxs-lookup"><span data-stu-id="f3c89-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="f3c89-115">Det andra kommandot får belastningsutjämnaren med namnet MyLB och skickar resultatet till cmdleten **Add-AzLoadBalancerFrontendIpConfig** som lägger till en front-IP-konfiguration till belastningsutjämnaren med en dynamisk privat IP-adress från det undernät som lagras i variabeln med namnet $MySubnet.</span><span class="sxs-lookup"><span data-stu-id="f3c89-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="f3c89-116">Exempel 2 lägga till en front-IP-konfiguration med en statisk IP-adress</span><span class="sxs-lookup"><span data-stu-id="f3c89-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="f3c89-117">Det första kommandot får det Azure Virtual Network som heter MyVnet och skickar resultatet med pipeline till cmdleten **Get-AzVirtualNetworkSubnetConfig** för att hämta under nätet med namnet mina undernät.</span><span class="sxs-lookup"><span data-stu-id="f3c89-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="f3c89-118">Då sparas resultatet i variabeln $Subnet.</span><span class="sxs-lookup"><span data-stu-id="f3c89-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="f3c89-119">Det andra kommandot får belastningsutjämnaren med namnet MyLB och skickar resultatet till cmdleten **Add-AzLoadBalancerFrontendIpConfig** som lägger till en front-IP-konfiguration till belastningsutjämnaren med en statisk privat IP-adress från det undernät som lagras i variabeln med namnet $Subnet.</span><span class="sxs-lookup"><span data-stu-id="f3c89-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="f3c89-120">Exempel 3 lägga till en front-IP-konfiguration med en offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="f3c89-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="f3c89-121">Det första kommandot får den offentliga Azure offentlige IP-adressen som heter MyPub och lagrar resultatet i variabeln som heter $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="f3c89-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="f3c89-122">Det andra kommandot får belastningsutjämnaren med namnet MyLB och skickar resultatet till cmdleten **Add-AzLoadBalancerFrontendIpConfig** som lägger till en front-IP-konfiguration till belastningsutjämnaren med offentlig IP-adress som lagras i variabeln som heter $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="f3c89-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="f3c89-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3c89-123">PARAMETERS</span></span>

### <span data-ttu-id="f3c89-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c89-124">-DefaultProfile</span></span>
<span data-ttu-id="f3c89-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f3c89-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3c89-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f3c89-126">-LoadBalancer</span></span>
<span data-ttu-id="f3c89-127">Anger ett **Loadbalancer** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f3c89-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="f3c89-128">Denna cmdlet lägger till en front-IP-konfiguration i belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f3c89-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c89-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="f3c89-129">-Name</span></span>
<span data-ttu-id="f3c89-130">Anger namnet på den frontend-IP-konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f3c89-130">Specifies the name of the front-end IP configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c89-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f3c89-131">-PrivateIpAddress</span></span>
<span data-ttu-id="f3c89-132">Anger den privata IP-adressen som ska kopplas till en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f3c89-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c89-133">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="f3c89-133">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="f3c89-134">Den privata IP-adressen för IP-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="f3c89-134">The private IP address version of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c89-135">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f3c89-135">-PublicIpAddress</span></span>
<span data-ttu-id="f3c89-136">Anger den offentliga IP-adressen som ska kopplas till en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f3c89-136">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c89-137">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="f3c89-137">-PublicIpAddressId</span></span>
<span data-ttu-id="f3c89-138">Anger ID för den offentliga IP-adressen som du vill lägga till en front-IP-konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="f3c89-138">Specifies the ID of the public IP address in which to add a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c89-139">-Undernät</span><span class="sxs-lookup"><span data-stu-id="f3c89-139">-Subnet</span></span>
<span data-ttu-id="f3c89-140">Anger det under näts objekt där en klient-IP-konfiguration ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f3c89-140">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c89-141">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f3c89-141">-SubnetId</span></span>
<span data-ttu-id="f3c89-142">Anger ID för det undernät där du vill lägga till en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f3c89-142">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c89-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="f3c89-143">-Zone</span></span>
<span data-ttu-id="f3c89-144">En lista över tillgänglighets zoner som betecknar den IP som tilldelats resursen måste komma från.</span><span class="sxs-lookup"><span data-stu-id="f3c89-144">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="f3c89-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f3c89-145">-Confirm</span></span>
<span data-ttu-id="f3c89-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f3c89-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c89-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3c89-147">-WhatIf</span></span>
<span data-ttu-id="f3c89-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f3c89-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3c89-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f3c89-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c89-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c89-150">CommonParameters</span></span>
<span data-ttu-id="f3c89-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3c89-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c89-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3c89-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c89-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3c89-153">INPUTS</span></span>

### <span data-ttu-id="f3c89-154">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f3c89-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="f3c89-155">System. String</span><span class="sxs-lookup"><span data-stu-id="f3c89-155">System.String</span></span>

### <span data-ttu-id="f3c89-156">System. string []</span><span class="sxs-lookup"><span data-stu-id="f3c89-156">System.String[]</span></span>

### <span data-ttu-id="f3c89-157">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="f3c89-157">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="f3c89-158">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f3c89-158">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="f3c89-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3c89-159">OUTPUTS</span></span>

### <span data-ttu-id="f3c89-160">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f3c89-160">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f3c89-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3c89-161">NOTES</span></span>

## <span data-ttu-id="f3c89-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3c89-162">RELATED LINKS</span></span>

[<span data-ttu-id="f3c89-163">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f3c89-163">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f3c89-164">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f3c89-164">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="f3c89-165">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f3c89-165">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f3c89-166">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f3c89-166">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f3c89-167">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f3c89-167">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f3c89-168">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f3c89-168">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


