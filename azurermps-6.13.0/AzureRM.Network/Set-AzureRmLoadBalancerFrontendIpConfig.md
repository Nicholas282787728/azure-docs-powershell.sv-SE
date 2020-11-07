---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 93313b6a2d9623ed518d6e79fabcda8fea5cc7b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755824"
---
# <span data-ttu-id="8b4a8-101">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8b4a8-101">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="8b4a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b4a8-102">SYNOPSIS</span></span>
<span data-ttu-id="8b4a8-103">Ställer in mål tillstånd för en front-IP-konfiguration i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b4a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b4a8-104">SYNTAX</span></span>

### <span data-ttu-id="8b4a8-105">SetByResourceSubnet (standard)</span><span class="sxs-lookup"><span data-stu-id="8b4a8-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b4a8-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="8b4a8-106">SetByResourceIdSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b4a8-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8b4a8-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b4a8-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8b4a8-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b4a8-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b4a8-109">DESCRIPTION</span></span>
<span data-ttu-id="8b4a8-110">Cmdleten **set-AzureRmLoadBalancerFrontendIpConfig** anger mål tillståndet för en front-IP-konfiguration i en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-110">The **Set-AzureRmLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="8b4a8-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b4a8-111">EXAMPLES</span></span>

### <span data-ttu-id="8b4a8-112">Exempel 1: ändra klient delens frontend-konfiguration för belastnings utjämning</span><span class="sxs-lookup"><span data-stu-id="8b4a8-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="8b4a8-113">Det första kommandot hämtar det virtuella under nätet med namnet Subnet och lagrar det sedan i $Subnet variabel.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="8b4a8-114">Det andra kommandot får den kopplade belastningsutjämnaren som heter MyLoadBalancer och lagrar den sedan i $slb variabel.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="8b4a8-115">I det tredje kommandot används pipeline-operatorn för att överföra belastningsutjämnaren i $slb till Add-AzureRmLoadBalancerFrontendIpConfig, som skapar en front-IP-konfiguration med namnet NewFrontend för $slb.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="8b4a8-116">Det fjärde kommandot skickar belastningsutjämnaren i $slb till **set-AzureRmLoadBalancerFrontendIpConfig** , som sparar och uppdaterar front-IP-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-116">The fourth command passes the load balancer in $slb to **Set-AzureRmLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="8b4a8-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b4a8-117">PARAMETERS</span></span>

### <span data-ttu-id="8b4a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b4a8-118">-DefaultProfile</span></span>
<span data-ttu-id="8b4a8-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b4a8-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8b4a8-120">-LoadBalancer</span></span>
<span data-ttu-id="8b4a8-121">Anger en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-121">Specifies a load balancer.</span></span>
<span data-ttu-id="8b4a8-122">Den här cmdleten ställer in mål tillstånd för en klient konfiguration för belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="8b4a8-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="8b4a8-123">-Name</span></span>
<span data-ttu-id="8b4a8-124">Anger namnet på den frontend-IP-konfiguration som ska ställas in.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="8b4a8-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="8b4a8-125">-PrivateIpAddress</span></span>
<span data-ttu-id="8b4a8-126">Anger den privata IP-adressen för belastningsutjämnaren som är kopplad till den frontend-IP-konfiguration som ska anges.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="8b4a8-127">Ange endast den här parametern om du också anger *under nätets* parameter.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="8b4a8-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8b4a8-128">-PublicIpAddress</span></span>
<span data-ttu-id="8b4a8-129">Anger det **PublicIpAddress** -objekt som är kopplat till den frontend-IP-konfiguration som ska anges.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="8b4a8-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="8b4a8-130">-PublicIpAddressId</span></span>
<span data-ttu-id="8b4a8-131">Anger ID för det **PublicIpAddress** -objekt som är kopplat till den front-end IP-konfiguration som denna cmdlet ställer in.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="8b4a8-132">-Undernät</span><span class="sxs-lookup"><span data-stu-id="8b4a8-132">-Subnet</span></span>
<span data-ttu-id="8b4a8-133">Anger det **Subnet** -objekt som innehåller den frontend-IP-konfiguration som denna cmdlet ställer in.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="8b4a8-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8b4a8-134">-SubnetId</span></span>
<span data-ttu-id="8b4a8-135">Anger ID för det undernät som innehåller den frontend-IP-konfiguration som denna cmdlet ställer in.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="8b4a8-136">-Zone</span><span class="sxs-lookup"><span data-stu-id="8b4a8-136">-Zone</span></span>
<span data-ttu-id="8b4a8-137">En lista över tillgänglighets zoner som betecknar den IP som tilldelats resursen måste komma från.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="8b4a8-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8b4a8-138">-Confirm</span></span>
<span data-ttu-id="8b4a8-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b4a8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b4a8-140">-WhatIf</span></span>
<span data-ttu-id="8b4a8-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b4a8-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b4a8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b4a8-143">CommonParameters</span></span>
<span data-ttu-id="8b4a8-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b4a8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b4a8-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b4a8-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b4a8-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b4a8-146">INPUTS</span></span>

### <span data-ttu-id="8b4a8-147">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8b4a8-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="8b4a8-148">Parametrar: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8b4a8-148">Parameters: LoadBalancer (ByValue)</span></span>

### <span data-ttu-id="8b4a8-149">System. Collections. Generic. list \` 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8b4a8-149">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="8b4a8-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b4a8-150">OUTPUTS</span></span>

### <span data-ttu-id="8b4a8-151">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8b4a8-151">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8b4a8-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b4a8-152">NOTES</span></span>

## <span data-ttu-id="8b4a8-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b4a8-153">RELATED LINKS</span></span>

[<span data-ttu-id="8b4a8-154">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8b4a8-154">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8b4a8-155">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8b4a8-155">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="8b4a8-156">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8b4a8-156">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8b4a8-157">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8b4a8-157">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="8b4a8-158">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8b4a8-158">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8b4a8-159">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8b4a8-159">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)


