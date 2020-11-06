---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 245129e314bc5fd9cfe81d6d9f218a011ffef55d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574819"
---
# <span data-ttu-id="4bb83-101">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4bb83-101">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="4bb83-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4bb83-102">SYNOPSIS</span></span>
<span data-ttu-id="4bb83-103">Lägger till en klient-IP-konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="4bb83-103">Adds a front-end IP configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bb83-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4bb83-104">SYNTAX</span></span>

### <span data-ttu-id="4bb83-105">SetByResourceSubnet (standard)</span><span class="sxs-lookup"><span data-stu-id="4bb83-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bb83-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="4bb83-106">SetByResourceIdSubnet</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bb83-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4bb83-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bb83-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4bb83-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bb83-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4bb83-109">DESCRIPTION</span></span>
<span data-ttu-id="4bb83-110">Cmdleten **Add-AzureRmLoadBalancerFrontendIpConifg** lägger till en klient-IP-konfiguration i en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="4bb83-110">The **Add-AzureRmLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="4bb83-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4bb83-111">EXAMPLES</span></span>

### <span data-ttu-id="4bb83-112">Exempel 1 lägga till en front-IP-konfiguration med en dynamisk IP-adress</span><span class="sxs-lookup"><span data-stu-id="4bb83-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzureRmLoadBalancer
```

<span data-ttu-id="4bb83-113">Det första kommandot får det Azure Virtual Network som heter MyVnet och skickar resultatet med pipeline till cmdleten **Get-AzureRmVirtualNetworkSubnetConfig** för att hämta under nätet med namnet mina undernät.</span><span class="sxs-lookup"><span data-stu-id="4bb83-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="4bb83-114">Då sparas resultatet i variabeln $Subnet.</span><span class="sxs-lookup"><span data-stu-id="4bb83-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="4bb83-115">Det andra kommandot får belastningsutjämnaren med namnet MyLB och skickar resultatet till cmdleten **Add-AzureRmLoadBalancerFrontendIpConfig** som lägger till en front-IP-konfiguration till belastningsutjämnaren med en dynamisk privat IP-adress från det undernät som lagras i variabeln med namnet $MySubnet.</span><span class="sxs-lookup"><span data-stu-id="4bb83-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="4bb83-116">Exempel 2 lägga till en front-IP-konfiguration med en statisk IP-adress</span><span class="sxs-lookup"><span data-stu-id="4bb83-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="4bb83-117">Det första kommandot får det Azure Virtual Network som heter MyVnet och skickar resultatet med pipeline till cmdleten **Get-AzureRmVirtualNetworkSubnetConfig** för att hämta under nätet med namnet mina undernät.</span><span class="sxs-lookup"><span data-stu-id="4bb83-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="4bb83-118">Då sparas resultatet i variabeln $Subnet.</span><span class="sxs-lookup"><span data-stu-id="4bb83-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="4bb83-119">Det andra kommandot får belastningsutjämnaren med namnet MyLB och skickar resultatet till cmdleten **Add-AzureRmLoadBalancerFrontendIpConfig** som lägger till en front-IP-konfiguration till belastningsutjämnaren med en statisk privat IP-adress från det undernät som lagras i variabeln med namnet $Subnet.</span><span class="sxs-lookup"><span data-stu-id="4bb83-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="4bb83-120">Exempel 3 lägga till en front-IP-konfiguration med en offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="4bb83-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzureRmPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzureRmLoadBalancer
```

<span data-ttu-id="4bb83-121">Det första kommandot får den offentliga Azure offentlige IP-adressen som heter MyPub och lagrar resultatet i variabeln som heter $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="4bb83-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="4bb83-122">Det andra kommandot får belastningsutjämnaren med namnet MyLB och skickar resultatet till cmdleten **Add-AzureRmLoadBalancerFrontendIpConfig** som lägger till en front-IP-konfiguration till belastningsutjämnaren med offentlig IP-adress som lagras i variabeln som heter $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="4bb83-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="4bb83-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4bb83-123">PARAMETERS</span></span>

### <span data-ttu-id="4bb83-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bb83-124">-DefaultProfile</span></span>
<span data-ttu-id="4bb83-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb83-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bb83-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4bb83-126">-LoadBalancer</span></span>
<span data-ttu-id="4bb83-127">Anger ett **Loadbalancer** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4bb83-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="4bb83-128">Denna cmdlet lägger till en front-IP-konfiguration i belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="4bb83-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="4bb83-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="4bb83-129">-Name</span></span>
<span data-ttu-id="4bb83-130">Anger namnet på den frontend-IP-konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="4bb83-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="4bb83-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="4bb83-131">-PrivateIpAddress</span></span>
<span data-ttu-id="4bb83-132">Anger den privata IP-adressen som ska kopplas till en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4bb83-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="4bb83-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4bb83-133">-PublicIpAddress</span></span>
<span data-ttu-id="4bb83-134">Anger den offentliga IP-adressen som ska kopplas till en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4bb83-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="4bb83-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="4bb83-135">-PublicIpAddressId</span></span>
<span data-ttu-id="4bb83-136">Specifes ID för den offentliga IP-adressen där en klient-IP-konfiguration ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="4bb83-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="4bb83-137">-Undernät</span><span class="sxs-lookup"><span data-stu-id="4bb83-137">-Subnet</span></span>
<span data-ttu-id="4bb83-138">Anger det under näts objekt där en klient-IP-konfiguration ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="4bb83-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="4bb83-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4bb83-139">-SubnetId</span></span>
<span data-ttu-id="4bb83-140">Anger ID för det undernät där du vill lägga till en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4bb83-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="4bb83-141">-Zone</span><span class="sxs-lookup"><span data-stu-id="4bb83-141">-Zone</span></span>
<span data-ttu-id="4bb83-142">En lista över tillgänglighets zoner som betecknar den IP som tilldelats resursen måste komma från.</span><span class="sxs-lookup"><span data-stu-id="4bb83-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="4bb83-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4bb83-143">-Confirm</span></span>
<span data-ttu-id="4bb83-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4bb83-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bb83-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bb83-145">-WhatIf</span></span>
<span data-ttu-id="4bb83-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4bb83-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4bb83-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4bb83-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bb83-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bb83-148">CommonParameters</span></span>
<span data-ttu-id="4bb83-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bb83-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bb83-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bb83-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bb83-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4bb83-151">INPUTS</span></span>

### <span data-ttu-id="4bb83-152">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4bb83-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="4bb83-153">Parametrar: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4bb83-153">Parameters: LoadBalancer (ByValue)</span></span>

### <span data-ttu-id="4bb83-154">System. Collections. Generic. list \` 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4bb83-154">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4bb83-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4bb83-155">OUTPUTS</span></span>

### <span data-ttu-id="4bb83-156">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4bb83-156">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4bb83-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4bb83-157">NOTES</span></span>

## <span data-ttu-id="4bb83-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4bb83-158">RELATED LINKS</span></span>

[<span data-ttu-id="4bb83-159">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4bb83-159">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4bb83-160">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4bb83-160">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="4bb83-161">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4bb83-161">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4bb83-162">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4bb83-162">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4bb83-163">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4bb83-163">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4bb83-164">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4bb83-164">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


