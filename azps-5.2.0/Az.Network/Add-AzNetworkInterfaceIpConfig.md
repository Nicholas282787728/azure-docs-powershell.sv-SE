---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 9fef4a3cfe57b75ad992d4f4068bb0d51bbdcd90
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410640"
---
# <span data-ttu-id="936d5-101">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="936d5-101">Add-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="936d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="936d5-102">SYNOPSIS</span></span>
<span data-ttu-id="936d5-103">Lägger till en IP-konfiguration för nätverks gränssnitt i ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="936d5-103">Adds a network interface IP configuration to a network interface.</span></span>

## <span data-ttu-id="936d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="936d5-104">SYNTAX</span></span>

### <span data-ttu-id="936d5-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="936d5-105">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="936d5-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="936d5-106">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="936d5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="936d5-107">DESCRIPTION</span></span>
<span data-ttu-id="936d5-108">Cmdleten **Add-AzNetworkInterfaceIpConfig** lägger till en IP-konfiguration för nätverks gränssnitt i ett Azure-nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="936d5-108">The **Add-AzNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="936d5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="936d5-109">EXAMPLES</span></span>

### <span data-ttu-id="936d5-110">Exempel 1: lägga till en ny IP-konfiguration med en program säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="936d5-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzVirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US" -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface
```

<span data-ttu-id="936d5-111">I det här exemplet skapar vi ett nytt nätverks gränssnitts-MyNetworkInterface som tillhör ett undernät i det nya virtuella nätverks MyVNET.</span><span class="sxs-lookup"><span data-stu-id="936d5-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="936d5-112">Vi skapar också en tom säkerhets grupp för program MyASG för att koppla samman med IP-konfigurationerna i nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="936d5-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="936d5-113">När båda objekten har skapats länkar vi standard-IP-konfigurationen till MyASG-objektet.</span><span class="sxs-lookup"><span data-stu-id="936d5-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="936d5-114">Nu skapar vi en ny IP-konfiguration i nätverks gränssnittet som också länka till program säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="936d5-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="936d5-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="936d5-115">PARAMETERS</span></span>

### <span data-ttu-id="936d5-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="936d5-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="936d5-117">Anger en samling med Programgateway-dataport-referenser som den här nätverks gränssnitts-IP-konfigurationen tillhör.</span><span class="sxs-lookup"><span data-stu-id="936d5-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="936d5-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="936d5-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="936d5-119">Anger en samling med Programgateway-dataport-referenser som den här nätverks gränssnitts-IP-konfigurationen tillhör.</span><span class="sxs-lookup"><span data-stu-id="936d5-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="936d5-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="936d5-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="936d5-121">Anger en samling med program säkerhets grupp referenser som denna IP-konfiguration för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="936d5-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="936d5-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="936d5-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="936d5-123">Anger en samling med program säkerhets grupp referenser som denna IP-konfiguration för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="936d5-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="936d5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="936d5-124">-DefaultProfile</span></span>
<span data-ttu-id="936d5-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="936d5-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="936d5-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="936d5-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="936d5-127">Anger en samling Server grupp referenser för belastnings utjämning som den här IP-konfigurationen för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="936d5-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="936d5-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="936d5-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="936d5-129">Anger en samling Server grupp referenser för belastnings utjämning som den här IP-konfigurationen för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="936d5-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="936d5-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="936d5-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="936d5-131">Anger en samling regel referenser för inkommande nätverks adresser (NAT) som den här nätverks gränssnitts-IP-konfigurationen tillhör.</span><span class="sxs-lookup"><span data-stu-id="936d5-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="936d5-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="936d5-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="936d5-133">Anger en mängd inkommande NAT-regler för belastnings utjämning som den här IP-konfigurationen för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="936d5-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="936d5-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="936d5-134">-Name</span></span>
<span data-ttu-id="936d5-135">Anger namnet på nätverks gränssnittets IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="936d5-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="936d5-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="936d5-136">-NetworkInterface</span></span>
<span data-ttu-id="936d5-137">Anger ett **NetworkInterface** -objekt.</span><span class="sxs-lookup"><span data-stu-id="936d5-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="936d5-138">Denna cmdlet lägger till en IP-konfiguration för nätverks gränssnitt till det objekt som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="936d5-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="936d5-139">-Primär</span><span class="sxs-lookup"><span data-stu-id="936d5-139">-Primary</span></span>
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

### <span data-ttu-id="936d5-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="936d5-140">-PrivateIpAddress</span></span>
<span data-ttu-id="936d5-141">Anger den statiska IP-adressen för nätverks gränssnittets IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="936d5-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="936d5-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="936d5-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="936d5-143">Anger IP-adressen för en IP-konfiguration för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="936d5-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="936d5-144">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="936d5-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="936d5-145">IPv4</span><span class="sxs-lookup"><span data-stu-id="936d5-145">IPv4</span></span>
- <span data-ttu-id="936d5-146">-</span><span class="sxs-lookup"><span data-stu-id="936d5-146">IPv6</span></span>

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

### <span data-ttu-id="936d5-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="936d5-147">-PublicIpAddress</span></span>
<span data-ttu-id="936d5-148">Anger ett **PublicIPAddress** -objekt.</span><span class="sxs-lookup"><span data-stu-id="936d5-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="936d5-149">Denna cmdlet skapar en referens till en offentlig IP-adress som ska kopplas till den här IP-konfigurationen för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="936d5-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="936d5-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="936d5-150">-PublicIpAddressId</span></span>
<span data-ttu-id="936d5-151">Denna cmdlet skapar en referens till en offentlig IP-adress som ska kopplas till den här IP-konfigurationen för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="936d5-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="936d5-152">-Undernät</span><span class="sxs-lookup"><span data-stu-id="936d5-152">-Subnet</span></span>
<span data-ttu-id="936d5-153">Anger ett **under näts** objekt.</span><span class="sxs-lookup"><span data-stu-id="936d5-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="936d5-154">Denna cmdlet skapar en referens till ett undernät där nätverks gränssnittets IP-konfiguration skapas.</span><span class="sxs-lookup"><span data-stu-id="936d5-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="936d5-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="936d5-155">-SubnetId</span></span>
<span data-ttu-id="936d5-156">Denna cmdlet skapar en referens till ett undernät där nätverks gränssnittets IP-konfiguration skapas.</span><span class="sxs-lookup"><span data-stu-id="936d5-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="936d5-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="936d5-157">CommonParameters</span></span>
<span data-ttu-id="936d5-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="936d5-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="936d5-159">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="936d5-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="936d5-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="936d5-160">INPUTS</span></span>

### <span data-ttu-id="936d5-161">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="936d5-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="936d5-162">System. string []</span><span class="sxs-lookup"><span data-stu-id="936d5-162">System.String[]</span></span>

### <span data-ttu-id="936d5-163">Microsoft. Azure. commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="936d5-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="936d5-164">Microsoft. Azure. commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="936d5-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="936d5-165">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="936d5-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="936d5-166">Microsoft. Azure. commands. Network. Models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="936d5-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="936d5-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="936d5-167">OUTPUTS</span></span>

### <span data-ttu-id="936d5-168">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="936d5-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="936d5-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="936d5-169">NOTES</span></span>
* <span data-ttu-id="936d5-170">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="936d5-170">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="936d5-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="936d5-171">RELATED LINKS</span></span>

[<span data-ttu-id="936d5-172">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="936d5-172">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="936d5-173">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="936d5-173">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="936d5-174">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="936d5-174">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="936d5-175">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="936d5-175">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
