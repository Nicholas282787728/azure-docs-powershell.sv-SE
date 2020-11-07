---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 4c65c2a37d877ec423850ade00115b4fe6c43798
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755826"
---
# <span data-ttu-id="63870-101">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="63870-101">New-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="63870-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63870-102">SYNOPSIS</span></span>
<span data-ttu-id="63870-103">Skapar en IP-konfiguration för nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="63870-103">Creates a network interface IP configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63870-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63870-104">SYNTAX</span></span>

### <span data-ttu-id="63870-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="63870-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63870-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="63870-106">SetByResourceId</span></span>
```
New-AzureRmNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63870-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63870-107">DESCRIPTION</span></span>
<span data-ttu-id="63870-108">Cmdleten **New-AzureRmNetworkInterfaceIpConfig** skapar en Azure-nätverks gränssnitts-IP-konfiguration för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="63870-108">The **New-AzureRmNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="63870-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63870-109">EXAMPLES</span></span>

### <span data-ttu-id="63870-110">1: skapa en IP-konfiguration med en offentlig IP-adress för ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="63870-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzureRmPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzureRmNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzureRmNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="63870-111">De två första kommandona får ett virtuellt nätverk som heter myvnet och ett under nätverk som har skapats tidigare.</span><span class="sxs-lookup"><span data-stu-id="63870-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="63870-112">Dessa lagras i $vnet och $Subnet.</span><span class="sxs-lookup"><span data-stu-id="63870-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="63870-113">Det tredje kommandot får en tidigare skapad offentlig IP-adress som heter PIP1.</span><span class="sxs-lookup"><span data-stu-id="63870-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="63870-114">Med kommandot tillbaka skapar du en ny IP-konfiguration med namnet "IPConfig-1" som primär IP-konfiguration med en offentlig IP-adress kopplad till sig.</span><span class="sxs-lookup"><span data-stu-id="63870-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="63870-115">Det senaste kommandot skapar sedan ett nätverks gränssnitt med namnet mynic1 med den här IP-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="63870-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="63870-116">2: skapa en IP-konfiguration med en privat IP-adress</span><span class="sxs-lookup"><span data-stu-id="63870-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzureRmNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzureRmNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="63870-117">De två första kommandona får ett virtuellt nätverk som heter myvnet och ett under nätverk som har skapats tidigare.</span><span class="sxs-lookup"><span data-stu-id="63870-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="63870-118">Dessa lagras i $vnet och $Subnet.</span><span class="sxs-lookup"><span data-stu-id="63870-118">These are stored in $vnet and $Subnet respectively.</span></span>  <span data-ttu-id="63870-119">Det tredje kommandot skapar en ny IP-konfiguration med namnet "IPConfig-2" med en privat IP-10.0.0.5 kopplad till sig.</span><span class="sxs-lookup"><span data-stu-id="63870-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="63870-120">Det senaste kommandot skapar sedan ett nätverks gränssnitt med namnet mynic1 med den här IP-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="63870-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="63870-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63870-121">PARAMETERS</span></span>

### <span data-ttu-id="63870-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="63870-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="63870-123">Anger en samling med Programgateway-dataport-referenser som den här nätverks gränssnitts-IP-konfigurationen tillhör.</span><span class="sxs-lookup"><span data-stu-id="63870-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63870-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="63870-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="63870-125">Anger en samling med Programgateway-dataport-referenser som den här nätverks gränssnitts-IP-konfigurationen tillhör.</span><span class="sxs-lookup"><span data-stu-id="63870-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63870-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="63870-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="63870-127">Anger en samling med program säkerhets grupp referenser som denna IP-konfiguration för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="63870-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63870-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="63870-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="63870-129">Anger en samling med program säkerhets grupp referenser som denna IP-konfiguration för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="63870-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63870-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63870-130">-DefaultProfile</span></span>
<span data-ttu-id="63870-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="63870-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63870-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="63870-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="63870-133">Anger en samling Server grupp referenser för belastnings utjämning som den här IP-konfigurationen för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="63870-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63870-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="63870-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="63870-135">Anger en samling Server grupp referenser för belastnings utjämning som den här IP-konfigurationen för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="63870-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63870-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="63870-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="63870-137">Anger en mängd inkommande NAT-regler för belastnings utjämning som nätverks gränssnittets IPConfiguration tillhör.</span><span class="sxs-lookup"><span data-stu-id="63870-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63870-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="63870-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="63870-139">Anger en samling regel referenser för inkommande nätverks adresser (NAT) som den här nätverks gränssnitts-IP-konfigurationen tillhör.</span><span class="sxs-lookup"><span data-stu-id="63870-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63870-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="63870-140">-Name</span></span>
<span data-ttu-id="63870-141">Anger namnet på nätverks gränssnittets IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="63870-141">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="63870-142">-Primär</span><span class="sxs-lookup"><span data-stu-id="63870-142">-Primary</span></span>
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

### <span data-ttu-id="63870-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="63870-143">-PrivateIpAddress</span></span>
<span data-ttu-id="63870-144">Anger den statiska IP-adressen för nätverks gränssnittets IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="63870-144">Specifies the static IP address of the network interface IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63870-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="63870-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="63870-146">Anger IP-adressen för en IP-konfiguration för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="63870-146">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="63870-147">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="63870-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="63870-148">IPv4</span><span class="sxs-lookup"><span data-stu-id="63870-148">IPv4</span></span>
- <span data-ttu-id="63870-149">-</span><span class="sxs-lookup"><span data-stu-id="63870-149">IPv6</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63870-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="63870-150">-PublicIpAddress</span></span>
<span data-ttu-id="63870-151">Anger ett **PublicIPAddress** -objekt.</span><span class="sxs-lookup"><span data-stu-id="63870-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="63870-152">Denna cmdlet skapar en referens till en offentlig IP-adress som ska kopplas till den här IP-konfigurationen för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="63870-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63870-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="63870-153">-PublicIpAddressId</span></span>
<span data-ttu-id="63870-154">Denna cmdlet skapar en referens till en offentlig IP-adress som ska kopplas till den här IP-konfigurationen för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="63870-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63870-155">-Undernät</span><span class="sxs-lookup"><span data-stu-id="63870-155">-Subnet</span></span>
<span data-ttu-id="63870-156">Anger ett **under näts** objekt.</span><span class="sxs-lookup"><span data-stu-id="63870-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="63870-157">Denna cmdlet skapar en referens till ett undernät där nätverks gränssnittets IP-konfiguration skapas.</span><span class="sxs-lookup"><span data-stu-id="63870-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63870-158">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="63870-158">-SubnetId</span></span>
<span data-ttu-id="63870-159">Anger en referens till ett undernät där nätverks gränssnittets IP-konfiguration skapas.</span><span class="sxs-lookup"><span data-stu-id="63870-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63870-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63870-160">CommonParameters</span></span>
<span data-ttu-id="63870-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63870-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63870-162">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63870-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63870-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63870-163">INPUTS</span></span>

### <span data-ttu-id="63870-164">System. Collections. Generic. list ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="63870-164">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="63870-165">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSBackendAddressPool, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="63870-165">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="63870-166">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSInboundNatRule, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="63870-166">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="63870-167">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewayBackendAddressPool, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="63870-167">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="63870-168">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationSecurityGroup, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="63870-168">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="63870-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63870-169">OUTPUTS</span></span>

### <span data-ttu-id="63870-170">Microsoft. Azure. commands. Networks. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="63870-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="63870-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63870-171">NOTES</span></span>
* <span data-ttu-id="63870-172">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="63870-172">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="63870-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63870-173">RELATED LINKS</span></span>

[<span data-ttu-id="63870-174">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="63870-174">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="63870-175">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="63870-175">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="63870-176">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="63870-176">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="63870-177">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="63870-177">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


