---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 62a479dd0c9c622100f5880c1aaf46836e179c53
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088397"
---
# <span data-ttu-id="e932e-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e932e-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="e932e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e932e-102">SYNOPSIS</span></span>
<span data-ttu-id="e932e-103">Uppdaterar en front-IP-konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e932e-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="e932e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e932e-104">SYNTAX</span></span>

### <span data-ttu-id="e932e-105">SetByResourceSubnet (standard)</span><span class="sxs-lookup"><span data-stu-id="e932e-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e932e-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="e932e-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e932e-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e932e-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e932e-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e932e-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e932e-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e932e-109">DESCRIPTION</span></span>
<span data-ttu-id="e932e-110">Cmdleten **set-AzLoadBalancerFrontendIpConfig** uppdaterar en front-IP-konfiguration för en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e932e-110">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="e932e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e932e-111">EXAMPLES</span></span>

### <span data-ttu-id="e932e-112">Exempel 1: ändra klient delens frontend-konfiguration för belastnings utjämning</span><span class="sxs-lookup"><span data-stu-id="e932e-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="e932e-113">Det första kommandot hämtar det virtuella under nätet med namnet Subnet och lagrar det sedan i $Subnet variabel.</span><span class="sxs-lookup"><span data-stu-id="e932e-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="e932e-114">Det andra kommandot får den kopplade belastningsutjämnaren som heter MyLoadBalancer och lagrar den sedan i $slb variabel.</span><span class="sxs-lookup"><span data-stu-id="e932e-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="e932e-115">I det tredje kommandot används pipeline-operatorn för att överföra belastningsutjämnaren i $slb till Add-AzLoadBalancerFrontendIpConfig, som skapar en front-IP-konfiguration med namnet NewFrontend för $slb.</span><span class="sxs-lookup"><span data-stu-id="e932e-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="e932e-116">Det fjärde kommandot skickar belastningsutjämnaren i $slb till **set-AzLoadBalancerFrontendIpConfig** , som sparar och uppdaterar front-IP-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="e932e-116">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="e932e-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e932e-117">PARAMETERS</span></span>

### <span data-ttu-id="e932e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e932e-118">-DefaultProfile</span></span>
<span data-ttu-id="e932e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e932e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e932e-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e932e-120">-LoadBalancer</span></span>
<span data-ttu-id="e932e-121">Anger en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="e932e-121">Specifies a load balancer.</span></span>
<span data-ttu-id="e932e-122">Denna cmdlet uppdaterar en klient konfiguration för belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e932e-122">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="e932e-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="e932e-123">-Name</span></span>
<span data-ttu-id="e932e-124">Anger namnet på den frontend-IP-konfiguration som ska ställas in.</span><span class="sxs-lookup"><span data-stu-id="e932e-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="e932e-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="e932e-125">-PrivateIpAddress</span></span>
<span data-ttu-id="e932e-126">Anger den privata IP-adressen för belastningsutjämnaren som är kopplad till den frontend-IP-konfiguration som ska anges.</span><span class="sxs-lookup"><span data-stu-id="e932e-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="e932e-127">Ange endast den här parametern om du också anger *under nätets* parameter.</span><span class="sxs-lookup"><span data-stu-id="e932e-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="e932e-128">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="e932e-128">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="e932e-129">Den privata IP-adressen för IP-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="e932e-129">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="e932e-130">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e932e-130">-PublicIpAddress</span></span>
<span data-ttu-id="e932e-131">Anger det **PublicIpAddress** -objekt som är kopplat till den frontend-IP-konfiguration som ska anges.</span><span class="sxs-lookup"><span data-stu-id="e932e-131">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="e932e-132">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="e932e-132">-PublicIpAddressId</span></span>
<span data-ttu-id="e932e-133">Anger ID för det **PublicIpAddress** -objekt som är kopplat till den front-end IP-konfiguration som denna cmdlet ställer in.</span><span class="sxs-lookup"><span data-stu-id="e932e-133">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="e932e-134">-Undernät</span><span class="sxs-lookup"><span data-stu-id="e932e-134">-Subnet</span></span>
<span data-ttu-id="e932e-135">Anger det **Subnet** -objekt som innehåller den frontend-IP-konfiguration som denna cmdlet ställer in.</span><span class="sxs-lookup"><span data-stu-id="e932e-135">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="e932e-136">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e932e-136">-SubnetId</span></span>
<span data-ttu-id="e932e-137">Anger ID för det undernät som innehåller den frontend-IP-konfiguration som denna cmdlet ställer in.</span><span class="sxs-lookup"><span data-stu-id="e932e-137">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="e932e-138">-Zone</span><span class="sxs-lookup"><span data-stu-id="e932e-138">-Zone</span></span>
<span data-ttu-id="e932e-139">En lista över tillgänglighets zoner som betecknar den IP som tilldelats resursen måste komma från.</span><span class="sxs-lookup"><span data-stu-id="e932e-139">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="e932e-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e932e-140">-Confirm</span></span>
<span data-ttu-id="e932e-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e932e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e932e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e932e-142">-WhatIf</span></span>
<span data-ttu-id="e932e-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e932e-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e932e-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e932e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e932e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e932e-145">CommonParameters</span></span>
<span data-ttu-id="e932e-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e932e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e932e-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e932e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e932e-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e932e-148">INPUTS</span></span>

### <span data-ttu-id="e932e-149">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e932e-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="e932e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="e932e-150">System.String</span></span>

### <span data-ttu-id="e932e-151">System. string []</span><span class="sxs-lookup"><span data-stu-id="e932e-151">System.String[]</span></span>

### <span data-ttu-id="e932e-152">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="e932e-152">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="e932e-153">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e932e-153">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="e932e-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e932e-154">OUTPUTS</span></span>

### <span data-ttu-id="e932e-155">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e932e-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e932e-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e932e-156">NOTES</span></span>

## <span data-ttu-id="e932e-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e932e-157">RELATED LINKS</span></span>

[<span data-ttu-id="e932e-158">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e932e-158">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="e932e-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e932e-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e932e-160">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e932e-160">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="e932e-161">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e932e-161">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="e932e-162">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e932e-162">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="e932e-163">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e932e-163">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


