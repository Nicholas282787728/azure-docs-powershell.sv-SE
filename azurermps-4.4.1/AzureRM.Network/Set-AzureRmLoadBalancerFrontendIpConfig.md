---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: d071e6f20d91dacfd99ca9566c64c4734ae93e31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575980"
---
# <span data-ttu-id="822bd-101">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="822bd-101">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="822bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="822bd-102">SYNOPSIS</span></span>
<span data-ttu-id="822bd-103">Ställer in mål tillstånd för en front-IP-konfiguration i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="822bd-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="822bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="822bd-104">SYNTAX</span></span>

### <span data-ttu-id="822bd-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="822bd-105">SetByResourceSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="822bd-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="822bd-106">SetByResourceIdSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="822bd-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="822bd-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="822bd-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="822bd-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="822bd-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="822bd-109">DESCRIPTION</span></span>
<span data-ttu-id="822bd-110">Cmdleten **set-AzureRmLoadBalancerFrontendIpConfig** anger mål tillståndet för en front-IP-konfiguration i en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="822bd-110">The **Set-AzureRmLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="822bd-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="822bd-111">EXAMPLES</span></span>

### <span data-ttu-id="822bd-112">Exempel 1: ändra klient delens frontend-konfiguration för belastnings utjämning</span><span class="sxs-lookup"><span data-stu-id="822bd-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="822bd-113">Det första kommandot hämtar det virtuella under nätet med namnet Subnet och lagrar det sedan i $Subnet variabel.</span><span class="sxs-lookup"><span data-stu-id="822bd-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>

<span data-ttu-id="822bd-114">Det andra kommandot får den kopplade belastningsutjämnaren som heter MyLoadBalancer och lagrar den sedan i $slb variabel.</span><span class="sxs-lookup"><span data-stu-id="822bd-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="822bd-115">I det tredje kommandot används pipeline-operatorn för att överföra belastningsutjämnaren i $slb till Add-AzureRmLoadBalancerFrontendIpConfig, som skapar en front-IP-konfiguration med namnet NewFrontend för $slb.</span><span class="sxs-lookup"><span data-stu-id="822bd-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>

<span data-ttu-id="822bd-116">Det fjärde kommandot skickar belastningsutjämnaren i $slb till **set-AzureRmLoadBalancerFrontendIpConfig** , som sparar och uppdaterar front-IP-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="822bd-116">The fourth command passes the load balancer in $slb to **Set-AzureRmLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="822bd-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="822bd-117">PARAMETERS</span></span>

### <span data-ttu-id="822bd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="822bd-118">-DefaultProfile</span></span>
<span data-ttu-id="822bd-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="822bd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="822bd-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="822bd-120">-LoadBalancer</span></span>
<span data-ttu-id="822bd-121">Anger en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="822bd-121">Specifies a load balancer.</span></span>
<span data-ttu-id="822bd-122">Den här cmdleten ställer in mål tillstånd för en klient konfiguration för belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="822bd-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="822bd-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="822bd-123">-Name</span></span>
<span data-ttu-id="822bd-124">Anger namnet på den frontend-IP-konfiguration som ska ställas in.</span><span class="sxs-lookup"><span data-stu-id="822bd-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="822bd-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="822bd-125">-PrivateIpAddress</span></span>
<span data-ttu-id="822bd-126">Anger den privata IP-adressen för belastningsutjämnaren som är kopplad till den frontend-IP-konfiguration som ska anges.</span><span class="sxs-lookup"><span data-stu-id="822bd-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="822bd-127">Ange endast den här parametern om du också anger *under nätets* parameter.</span><span class="sxs-lookup"><span data-stu-id="822bd-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="822bd-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="822bd-128">-PublicIpAddress</span></span>
<span data-ttu-id="822bd-129">Anger det **PublicIpAddress** -objekt som är kopplat till den frontend-IP-konfiguration som ska anges.</span><span class="sxs-lookup"><span data-stu-id="822bd-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="822bd-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="822bd-130">-PublicIpAddressId</span></span>
<span data-ttu-id="822bd-131">Anger ID för det **PublicIpAddress** -objekt som är kopplat till den front-end IP-konfiguration som denna cmdlet ställer in.</span><span class="sxs-lookup"><span data-stu-id="822bd-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="822bd-132">-Undernät</span><span class="sxs-lookup"><span data-stu-id="822bd-132">-Subnet</span></span>
<span data-ttu-id="822bd-133">Anger det **Subnet** -objekt som innehåller den frontend-IP-konfiguration som denna cmdlet ställer in.</span><span class="sxs-lookup"><span data-stu-id="822bd-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="822bd-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="822bd-134">-SubnetId</span></span>
<span data-ttu-id="822bd-135">Anger ID för det undernät som innehåller den frontend-IP-konfiguration som denna cmdlet ställer in.</span><span class="sxs-lookup"><span data-stu-id="822bd-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="822bd-136">-Zone</span><span class="sxs-lookup"><span data-stu-id="822bd-136">-Zone</span></span>
<span data-ttu-id="822bd-137">En lista över tillgänglighets zoner som betecknar den IP som tilldelats resursen måste komma från.</span><span class="sxs-lookup"><span data-stu-id="822bd-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="822bd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="822bd-138">CommonParameters</span></span>
<span data-ttu-id="822bd-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="822bd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="822bd-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="822bd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="822bd-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="822bd-141">INPUTS</span></span>

### <span data-ttu-id="822bd-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="822bd-142">PSLoadBalancer</span></span>
<span data-ttu-id="822bd-143">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="822bd-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="822bd-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="822bd-144">OUTPUTS</span></span>

### <span data-ttu-id="822bd-145">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="822bd-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="822bd-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="822bd-146">NOTES</span></span>

## <span data-ttu-id="822bd-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="822bd-147">RELATED LINKS</span></span>

[<span data-ttu-id="822bd-148">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="822bd-148">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="822bd-149">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="822bd-149">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="822bd-150">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="822bd-150">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="822bd-151">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="822bd-151">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="822bd-152">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="822bd-152">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="822bd-153">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="822bd-153">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)


