---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 57c92345537e72a38c5228c0a10d38f6ad61d13a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585451"
---
# <span data-ttu-id="e1494-101">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e1494-101">Add-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="e1494-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1494-102">SYNOPSIS</span></span>
<span data-ttu-id="e1494-103">Lägger till en IP-konfiguration för nätverks gränssnitt i ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="e1494-103">Adds a network interface IP configuration to a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1494-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1494-104">SYNTAX</span></span>

### <span data-ttu-id="e1494-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="e1494-105">SetByResource (Default)</span></span>
```
Add-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1494-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e1494-106">SetByResourceId</span></span>
```
Add-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1494-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1494-107">DESCRIPTION</span></span>
<span data-ttu-id="e1494-108">Cmdleten **Add-AzureRmNetworkInterfaceIpConfig** lägger till en IP-konfiguration för nätverks gränssnitt i ett Azure-nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="e1494-108">The **Add-AzureRmNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="e1494-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1494-109">EXAMPLES</span></span>

### <span data-ttu-id="e1494-110">Exempel 1: lägga till en ny IP-konfiguration med en program säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="e1494-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzureRmvirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzureRmNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US"  -Subnet $vnet.Subnets[0]

$asg = New-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzureRmNetworkInterface

$nic | Add-AzureRmNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg  | Set-AzureRmNetworkInterface
```

<span data-ttu-id="e1494-111">I det här exemplet skapar vi ett nytt nätverks gränssnitts-MyNetworkInterface som tillhör ett undernät i det nya virtuella nätverks MyVNET.</span><span class="sxs-lookup"><span data-stu-id="e1494-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="e1494-112">Vi skapar också en tom säkerhets grupp för program MyASG för att koppla samman med IP-konfigurationerna i nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="e1494-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="e1494-113">När båda objekten har skapats länkar vi standard-IP-konfigurationen till MyASG-objektet.</span><span class="sxs-lookup"><span data-stu-id="e1494-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="e1494-114">Nu skapar vi en ny IP-konfiguration i nätverks gränssnittet som också länka till program säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="e1494-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="e1494-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1494-115">PARAMETERS</span></span>

### <span data-ttu-id="e1494-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e1494-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="e1494-117">Anger en samling med Programgateway-dataport-referenser som den här nätverks gränssnitts-IP-konfigurationen tillhör.</span><span class="sxs-lookup"><span data-stu-id="e1494-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e1494-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e1494-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="e1494-119">Anger en samling med Programgateway-dataport-referenser som den här nätverks gränssnitts-IP-konfigurationen tillhör.</span><span class="sxs-lookup"><span data-stu-id="e1494-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e1494-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e1494-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="e1494-121">Anger en samling med program säkerhets grupp referenser som denna IP-konfiguration för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="e1494-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e1494-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e1494-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="e1494-123">Anger en samling med program säkerhets grupp referenser som denna IP-konfiguration för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="e1494-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e1494-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1494-124">-DefaultProfile</span></span>
<span data-ttu-id="e1494-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e1494-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1494-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e1494-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="e1494-127">Anger en samling Server grupp referenser för belastnings utjämning som den här IP-konfigurationen för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="e1494-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e1494-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e1494-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="e1494-129">Anger en samling Server grupp referenser för belastnings utjämning som den här IP-konfigurationen för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="e1494-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e1494-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="e1494-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="e1494-131">Anger en samling regel referenser för inkommande nätverks adresser (NAT) som den här nätverks gränssnitts-IP-konfigurationen tillhör.</span><span class="sxs-lookup"><span data-stu-id="e1494-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e1494-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="e1494-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="e1494-133">Anger en mängd inkommande NAT-regler för belastnings utjämning som den här IP-konfigurationen för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="e1494-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="e1494-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="e1494-134">-Name</span></span>
<span data-ttu-id="e1494-135">Anger namnet på nätverks gränssnittets IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e1494-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="e1494-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e1494-136">-NetworkInterface</span></span>
<span data-ttu-id="e1494-137">Anger ett **NetworkInterface** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e1494-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="e1494-138">Denna cmdlet lägger till en IP-konfiguration för nätverks gränssnitt till det objekt som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e1494-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="e1494-139">-Primär</span><span class="sxs-lookup"><span data-stu-id="e1494-139">-Primary</span></span>
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

### <span data-ttu-id="e1494-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="e1494-140">-PrivateIpAddress</span></span>
<span data-ttu-id="e1494-141">Anger den statiska IP-adressen för nätverks gränssnittets IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e1494-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="e1494-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="e1494-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="e1494-143">Anger IP-adressen för en IP-konfiguration för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="e1494-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="e1494-144">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e1494-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e1494-145">IPv4</span><span class="sxs-lookup"><span data-stu-id="e1494-145">IPv4</span></span>
- <span data-ttu-id="e1494-146">-</span><span class="sxs-lookup"><span data-stu-id="e1494-146">IPv6</span></span>

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

### <span data-ttu-id="e1494-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e1494-147">-PublicIpAddress</span></span>
<span data-ttu-id="e1494-148">Anger ett **PublicIPAddress** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e1494-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="e1494-149">Denna cmdlet skapar en referens till en offentlig IP-adress som ska kopplas till den här IP-konfigurationen för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="e1494-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="e1494-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="e1494-150">-PublicIpAddressId</span></span>
<span data-ttu-id="e1494-151">Denna cmdlet skapar en referens till en offentlig IP-adress som ska kopplas till den här IP-konfigurationen för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="e1494-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="e1494-152">-Undernät</span><span class="sxs-lookup"><span data-stu-id="e1494-152">-Subnet</span></span>
<span data-ttu-id="e1494-153">Anger ett **under näts** objekt.</span><span class="sxs-lookup"><span data-stu-id="e1494-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="e1494-154">Denna cmdlet skapar en referens till ett undernät där nätverks gränssnittets IP-konfiguration skapas.</span><span class="sxs-lookup"><span data-stu-id="e1494-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="e1494-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e1494-155">-SubnetId</span></span>
<span data-ttu-id="e1494-156">Denna cmdlet skapar en referens till ett undernät där nätverks gränssnittets IP-konfiguration skapas.</span><span class="sxs-lookup"><span data-stu-id="e1494-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="e1494-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1494-157">CommonParameters</span></span>
<span data-ttu-id="e1494-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1494-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1494-159">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1494-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1494-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1494-160">INPUTS</span></span>

### <span data-ttu-id="e1494-161">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e1494-161">PSNetworkInterface</span></span>
<span data-ttu-id="e1494-162">Parametern ' NetworkInterface ' godkänner värdet av typen ' PSNetworkInterface ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e1494-162">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="e1494-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1494-163">OUTPUTS</span></span>

### <span data-ttu-id="e1494-164">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e1494-164">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="e1494-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1494-165">NOTES</span></span>
* <span data-ttu-id="e1494-166">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="e1494-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e1494-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1494-167">RELATED LINKS</span></span>

[<span data-ttu-id="e1494-168">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e1494-168">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e1494-169">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e1494-169">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e1494-170">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e1494-170">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e1494-171">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e1494-171">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


