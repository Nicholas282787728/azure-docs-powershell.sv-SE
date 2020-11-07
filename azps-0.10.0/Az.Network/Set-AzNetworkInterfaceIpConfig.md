---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 0e74aa06d2966ed4e907de7428ddc1f4d3a6f2cb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924189"
---
# <span data-ttu-id="21e6d-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="21e6d-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="21e6d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="21e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="21e6d-103">Anger mål tillstånd för en Azure-nätverks gränssnitts-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="21e6d-103">Sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="21e6d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="21e6d-104">SYNTAX</span></span>

### <span data-ttu-id="21e6d-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="21e6d-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21e6d-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="21e6d-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21e6d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="21e6d-107">DESCRIPTION</span></span>
<span data-ttu-id="21e6d-108">Cmdleten **set-AzNetworkInterfaceIpConfig** anger mål tillståndet för en IP-konfiguration för Azure-nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="21e6d-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="21e6d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="21e6d-109">EXAMPLES</span></span>

### <span data-ttu-id="21e6d-110">1: ändra IP-adressen för en IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="21e6d-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="21e6d-111">De två första kommandona får ett virtuellt nätverk som heter myvnet och ett under nätverk som heter mina undernät och lagrar det i variabel $vnet och $subnet.</span><span class="sxs-lookup"><span data-stu-id="21e6d-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="21e6d-112">Det tredje kommandot får nätverks gränssnittet NIC1 associerat med den IP-konfiguration som måste uppdateras.</span><span class="sxs-lookup"><span data-stu-id="21e6d-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="21e6d-113">Det tredje kommandot anger den privata IP-adressen för den primära IP-ipconfig1 till 10.0.0.11.</span><span class="sxs-lookup"><span data-stu-id="21e6d-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="21e6d-114">Slutligen uppdaterar det senaste kommandot nätverks gränssnittet att ändringarna har genomförts.</span><span class="sxs-lookup"><span data-stu-id="21e6d-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="21e6d-115">2: associera en IP-konfiguration med en säkerhets groupp för ett program</span><span class="sxs-lookup"><span data-stu-id="21e6d-115">2: Associating an IP configuration with an applicaiton security groupp</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="21e6d-116">I det här exemplet innehåller variabeln $asg en referens till en program säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="21e6d-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="21e6d-117">Det fjärde kommandot får nätverks gränssnittet NIC1 associerat med den IP-konfiguration som måste uppdateras.</span><span class="sxs-lookup"><span data-stu-id="21e6d-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="21e6d-118">Set-AzNetworkInterfaceIpConfig anger den privata IP-adressen för den primära IP-konfigurationen för ipconfig1 till 10.0.0.11 och skapar en associering med den säkerhets gruppen för hämtade program.</span><span class="sxs-lookup"><span data-stu-id="21e6d-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="21e6d-119">Slutligen uppdaterar det senaste kommandot nätverks gränssnittet att ändringarna har genomförts.</span><span class="sxs-lookup"><span data-stu-id="21e6d-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="21e6d-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="21e6d-120">PARAMETERS</span></span>

### <span data-ttu-id="21e6d-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="21e6d-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="21e6d-122">Anger en samling med Programgateway-dataport-referenser som den här nätverks gränssnitts-IP-konfigurationen tillhör.</span><span class="sxs-lookup"><span data-stu-id="21e6d-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="21e6d-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="21e6d-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="21e6d-124">Anger en samling med Programgateway-dataport-referenser som den här nätverks gränssnitts-IP-konfigurationen tillhör.</span><span class="sxs-lookup"><span data-stu-id="21e6d-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="21e6d-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="21e6d-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="21e6d-126">Anger en samling med program säkerhets grupp referenser som denna IP-konfiguration för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="21e6d-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="21e6d-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="21e6d-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="21e6d-128">Anger en samling med program säkerhets grupp referenser som denna IP-konfiguration för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="21e6d-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="21e6d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21e6d-129">-DefaultProfile</span></span>
<span data-ttu-id="21e6d-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="21e6d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e6d-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="21e6d-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="21e6d-132">Anger en samling Server grupp referenser för belastnings utjämning som den här IP-konfigurationen för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="21e6d-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="21e6d-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="21e6d-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="21e6d-134">Anger en samling Server grupp referenser för belastnings utjämning som den här IP-konfigurationen för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="21e6d-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="21e6d-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="21e6d-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="21e6d-136">Anger en samling regel referenser för inkommande nätverks adresser (NAT) som den här nätverks gränssnitts-IP-konfigurationen tillhör.</span><span class="sxs-lookup"><span data-stu-id="21e6d-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="21e6d-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="21e6d-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="21e6d-138">Anger en mängd inkommande NAT-regler för belastnings utjämning som den här IP-konfigurationen för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="21e6d-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="21e6d-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="21e6d-139">-Name</span></span>
<span data-ttu-id="21e6d-140">Anger namnet på den nätverks-IP-konfiguration som cmdleten ställer in.</span><span class="sxs-lookup"><span data-stu-id="21e6d-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e6d-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="21e6d-141">-NetworkInterface</span></span>
<span data-ttu-id="21e6d-142">Anger ett **NetworkInterface** -objekt.</span><span class="sxs-lookup"><span data-stu-id="21e6d-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="21e6d-143">Denna cmdlet lägger till en IP-konfiguration för nätverks gränssnitt till det objekt som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="21e6d-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21e6d-144">-Primär</span><span class="sxs-lookup"><span data-stu-id="21e6d-144">-Primary</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e6d-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="21e6d-145">-PrivateIpAddress</span></span>
<span data-ttu-id="21e6d-146">Anger den statiska IP-adressen för nätverks gränssnittets IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="21e6d-146">Specifies the static IP address of the network interface IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e6d-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="21e6d-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="21e6d-148">Anger IP-adressen för en IP-konfiguration för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="21e6d-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="21e6d-149">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="21e6d-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="21e6d-150">IPv4</span><span class="sxs-lookup"><span data-stu-id="21e6d-150">IPv4</span></span>
- <span data-ttu-id="21e6d-151">-</span><span class="sxs-lookup"><span data-stu-id="21e6d-151">IPv6</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e6d-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="21e6d-152">-PublicIpAddress</span></span>
<span data-ttu-id="21e6d-153">Anger ett **PublicIPAddress** -objekt.</span><span class="sxs-lookup"><span data-stu-id="21e6d-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="21e6d-154">Denna cmdlet skapar en referens till en offentlig IP-adress som ska kopplas till den här IP-konfigurationen för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="21e6d-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e6d-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="21e6d-155">-PublicIpAddressId</span></span>
<span data-ttu-id="21e6d-156">Denna cmdlet skapar en referens till en offentlig IP-adress som ska kopplas till den här IP-konfigurationen för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="21e6d-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e6d-157">-Undernät</span><span class="sxs-lookup"><span data-stu-id="21e6d-157">-Subnet</span></span>
<span data-ttu-id="21e6d-158">Anger ett **under näts** objekt.</span><span class="sxs-lookup"><span data-stu-id="21e6d-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="21e6d-159">Denna cmdlet skapar en referens till ett undernät där nätverks gränssnittets IP-konfiguration skapas.</span><span class="sxs-lookup"><span data-stu-id="21e6d-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e6d-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="21e6d-160">-SubnetId</span></span>
<span data-ttu-id="21e6d-161">Denna cmdlet skapar en referens till ett undernät där nätverks gränssnittets IP-konfiguration skapas.</span><span class="sxs-lookup"><span data-stu-id="21e6d-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e6d-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21e6d-162">CommonParameters</span></span>
<span data-ttu-id="21e6d-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21e6d-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21e6d-164">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21e6d-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21e6d-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="21e6d-165">INPUTS</span></span>

### <span data-ttu-id="21e6d-166">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="21e6d-166">PSNetworkInterface</span></span>
<span data-ttu-id="21e6d-167">Parametern ' NetworkInterface ' godkänner värdet av typen ' PSNetworkInterface ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="21e6d-167">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="21e6d-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="21e6d-168">OUTPUTS</span></span>

### <span data-ttu-id="21e6d-169">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="21e6d-169">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="21e6d-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="21e6d-170">NOTES</span></span>
* <span data-ttu-id="21e6d-171">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="21e6d-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="21e6d-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="21e6d-172">RELATED LINKS</span></span>

[<span data-ttu-id="21e6d-173">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="21e6d-173">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="21e6d-174">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="21e6d-174">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="21e6d-175">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="21e6d-175">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="21e6d-176">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="21e6d-176">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)


