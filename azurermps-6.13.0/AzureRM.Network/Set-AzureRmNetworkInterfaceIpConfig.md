---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8804fd7fd9e2ea1d784d2b1607f72e7e0aa1bb6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572707"
---
# <span data-ttu-id="b137a-101">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b137a-101">Set-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="b137a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b137a-102">SYNOPSIS</span></span>
<span data-ttu-id="b137a-103">Anger mål tillstånd för en Azure-nätverks gränssnitts-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b137a-103">Sets the goal state for an Azure network interface IP configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b137a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b137a-104">SYNTAX</span></span>

### <span data-ttu-id="b137a-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="b137a-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b137a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b137a-106">SetByResourceId</span></span>
```
Set-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b137a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b137a-107">DESCRIPTION</span></span>
<span data-ttu-id="b137a-108">Cmdleten **set-AzureRmNetworkInterfaceIpConfig** anger mål tillståndet för en IP-konfiguration för Azure-nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="b137a-108">The **Set-AzureRmNetworkInterfaceIpConfig** cmdlet sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="b137a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b137a-109">EXAMPLES</span></span>

### <span data-ttu-id="b137a-110">1: ändra IP-adressen för en IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="b137a-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="b137a-111">De två första kommandona får ett virtuellt nätverk som heter myvnet och ett under nätverk som heter mina undernät och lagrar det i variabel $vnet och $subnet.</span><span class="sxs-lookup"><span data-stu-id="b137a-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="b137a-112">Det tredje kommandot får nätverks gränssnittet NIC1 associerat med den IP-konfiguration som måste uppdateras.</span><span class="sxs-lookup"><span data-stu-id="b137a-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="b137a-113">Det tredje kommandot anger den privata IP-adressen för den primära IP-ipconfig1 till 10.0.0.11.</span><span class="sxs-lookup"><span data-stu-id="b137a-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="b137a-114">Slutligen uppdaterar det senaste kommandot nätverks gränssnittet att ändringarna har genomförts.</span><span class="sxs-lookup"><span data-stu-id="b137a-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="b137a-115">2: associera en IP-konfiguration med en säkerhets grupp för program</span><span class="sxs-lookup"><span data-stu-id="b137a-115">2: Associating an IP configuration with an application security group</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="b137a-116">I det här exemplet innehåller variabeln $asg en referens till en program säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="b137a-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="b137a-117">Det fjärde kommandot får nätverks gränssnittet NIC1 associerat med den IP-konfiguration som måste uppdateras.</span><span class="sxs-lookup"><span data-stu-id="b137a-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="b137a-118">Set-AzureRmNetworkInterfaceIpConfig anger den privata IP-adressen för den primära IP-konfigurationen för ipconfig1 till 10.0.0.11 och skapar en associering med den säkerhets gruppen för hämtade program.</span><span class="sxs-lookup"><span data-stu-id="b137a-118">The Set-AzureRmNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="b137a-119">Slutligen uppdaterar det senaste kommandot nätverks gränssnittet att ändringarna har genomförts.</span><span class="sxs-lookup"><span data-stu-id="b137a-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="b137a-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b137a-120">PARAMETERS</span></span>

### <span data-ttu-id="b137a-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b137a-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="b137a-122">Anger en samling med Programgateway-dataport-referenser som den här nätverks gränssnitts-IP-konfigurationen tillhör.</span><span class="sxs-lookup"><span data-stu-id="b137a-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b137a-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b137a-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="b137a-124">Anger en samling med Programgateway-dataport-referenser som den här nätverks gränssnitts-IP-konfigurationen tillhör.</span><span class="sxs-lookup"><span data-stu-id="b137a-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b137a-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b137a-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="b137a-126">Anger en samling med program säkerhets grupp referenser som denna IP-konfiguration för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="b137a-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b137a-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b137a-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="b137a-128">Anger en samling med program säkerhets grupp referenser som denna IP-konfiguration för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="b137a-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b137a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b137a-129">-DefaultProfile</span></span>
<span data-ttu-id="b137a-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b137a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b137a-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b137a-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="b137a-132">Anger en samling Server grupp referenser för belastnings utjämning som den här IP-konfigurationen för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="b137a-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b137a-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b137a-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="b137a-134">Anger en samling Server grupp referenser för belastnings utjämning som den här IP-konfigurationen för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="b137a-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b137a-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="b137a-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="b137a-136">Anger en samling regel referenser för inkommande nätverks adresser (NAT) som den här nätverks gränssnitts-IP-konfigurationen tillhör.</span><span class="sxs-lookup"><span data-stu-id="b137a-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b137a-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="b137a-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="b137a-138">Anger en mängd inkommande NAT-regler för belastnings utjämning som den här IP-konfigurationen för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="b137a-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b137a-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="b137a-139">-Name</span></span>
<span data-ttu-id="b137a-140">Anger namnet på den nätverks-IP-konfiguration som cmdleten ställer in.</span><span class="sxs-lookup"><span data-stu-id="b137a-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="b137a-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b137a-141">-NetworkInterface</span></span>
<span data-ttu-id="b137a-142">Anger ett **NetworkInterface** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b137a-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="b137a-143">Denna cmdlet lägger till en IP-konfiguration för nätverks gränssnitt till det objekt som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b137a-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b137a-144">-Primär</span><span class="sxs-lookup"><span data-stu-id="b137a-144">-Primary</span></span>
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

### <span data-ttu-id="b137a-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="b137a-145">-PrivateIpAddress</span></span>
<span data-ttu-id="b137a-146">Anger den statiska IP-adressen för nätverks gränssnittets IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b137a-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="b137a-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="b137a-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="b137a-148">Anger IP-adressen för en IP-konfiguration för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="b137a-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="b137a-149">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b137a-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b137a-150">IPv4</span><span class="sxs-lookup"><span data-stu-id="b137a-150">IPv4</span></span>
- <span data-ttu-id="b137a-151">-</span><span class="sxs-lookup"><span data-stu-id="b137a-151">IPv6</span></span>

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

### <span data-ttu-id="b137a-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b137a-152">-PublicIpAddress</span></span>
<span data-ttu-id="b137a-153">Anger ett **PublicIPAddress** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b137a-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="b137a-154">Denna cmdlet skapar en referens till en offentlig IP-adress som ska kopplas till den här IP-konfigurationen för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="b137a-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="b137a-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="b137a-155">-PublicIpAddressId</span></span>
<span data-ttu-id="b137a-156">Denna cmdlet skapar en referens till en offentlig IP-adress som ska kopplas till den här IP-konfigurationen för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="b137a-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="b137a-157">-Undernät</span><span class="sxs-lookup"><span data-stu-id="b137a-157">-Subnet</span></span>
<span data-ttu-id="b137a-158">Anger ett **under näts** objekt.</span><span class="sxs-lookup"><span data-stu-id="b137a-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="b137a-159">Denna cmdlet skapar en referens till ett undernät där nätverks gränssnittets IP-konfiguration skapas.</span><span class="sxs-lookup"><span data-stu-id="b137a-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="b137a-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b137a-160">-SubnetId</span></span>
<span data-ttu-id="b137a-161">Denna cmdlet skapar en referens till ett undernät där nätverks gränssnittets IP-konfiguration skapas.</span><span class="sxs-lookup"><span data-stu-id="b137a-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="b137a-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b137a-162">CommonParameters</span></span>
<span data-ttu-id="b137a-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b137a-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b137a-164">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b137a-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b137a-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b137a-165">INPUTS</span></span>

### <span data-ttu-id="b137a-166">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b137a-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>
<span data-ttu-id="b137a-167">Parametrar: NetworkInterface (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b137a-167">Parameters: NetworkInterface (ByValue)</span></span>

### <span data-ttu-id="b137a-168">System. Collections. Generic. list ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b137a-168">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b137a-169">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSBackendAddressPool, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b137a-169">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="b137a-170">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSInboundNatRule, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b137a-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="b137a-171">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewayBackendAddressPool, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b137a-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="b137a-172">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationSecurityGroup, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b137a-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b137a-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b137a-173">OUTPUTS</span></span>

### <span data-ttu-id="b137a-174">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b137a-174">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="b137a-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b137a-175">NOTES</span></span>
* <span data-ttu-id="b137a-176">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="b137a-176">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b137a-177">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b137a-177">RELATED LINKS</span></span>

[<span data-ttu-id="b137a-178">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b137a-178">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b137a-179">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b137a-179">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b137a-180">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b137a-180">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b137a-181">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b137a-181">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)


