---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 6bf01750543fa5564e9490ad85d84cc258f10f4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755661"
---
# <span data-ttu-id="eb17c-101">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="eb17c-101">Set-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="eb17c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb17c-102">SYNOPSIS</span></span>
<span data-ttu-id="eb17c-103">Anger mål tillstånd för en Azure-nätverks gränssnitts-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="eb17c-103">Sets the goal state for an Azure network interface IP configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb17c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb17c-104">SYNTAX</span></span>

### <span data-ttu-id="eb17c-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="eb17c-105">SetByResource (Default)</span></span>
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

### <span data-ttu-id="eb17c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="eb17c-106">SetByResourceId</span></span>
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

## <span data-ttu-id="eb17c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb17c-107">DESCRIPTION</span></span>
<span data-ttu-id="eb17c-108">Cmdleten **set-AzureRmNetworkInterfaceIpConfig** anger mål tillståndet för en IP-konfiguration för Azure-nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="eb17c-108">The **Set-AzureRmNetworkInterfaceIpConfig** cmdlet sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="eb17c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb17c-109">EXAMPLES</span></span>

### <span data-ttu-id="eb17c-110">1: ändra IP-adressen för en IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="eb17c-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="eb17c-111">De två första kommandona får ett virtuellt nätverk som heter myvnet och ett under nätverk som heter mina undernät och lagrar det i variabel $vnet och $subnet.</span><span class="sxs-lookup"><span data-stu-id="eb17c-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="eb17c-112">Det tredje kommandot får nätverks gränssnittet NIC1 associerat med den IP-konfiguration som måste uppdateras.</span><span class="sxs-lookup"><span data-stu-id="eb17c-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="eb17c-113">Det tredje kommandot anger den privata IP-adressen för den primära IP-ipconfig1 till 10.0.0.11.</span><span class="sxs-lookup"><span data-stu-id="eb17c-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="eb17c-114">Slutligen uppdaterar det senaste kommandot nätverks gränssnittet att ändringarna har genomförts.</span><span class="sxs-lookup"><span data-stu-id="eb17c-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="eb17c-115">2: associera en IP-konfiguration med en säkerhets groupp för ett program</span><span class="sxs-lookup"><span data-stu-id="eb17c-115">2: Associating an IP configuration with an applicaiton security groupp</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="eb17c-116">I det här exemplet innehåller variabeln $asg en referens till en program säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="eb17c-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="eb17c-117">Det fjärde kommandot får nätverks gränssnittet NIC1 associerat med den IP-konfiguration som måste uppdateras.</span><span class="sxs-lookup"><span data-stu-id="eb17c-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="eb17c-118">Set-AzureRmNetworkInterfaceIpConfig anger den privata IP-adressen för den primära IP-konfigurationen för ipconfig1 till 10.0.0.11 och skapar en associering med den säkerhets gruppen för hämtade program.</span><span class="sxs-lookup"><span data-stu-id="eb17c-118">The Set-AzureRmNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="eb17c-119">Slutligen uppdaterar det senaste kommandot nätverks gränssnittet att ändringarna har genomförts.</span><span class="sxs-lookup"><span data-stu-id="eb17c-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="eb17c-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb17c-120">PARAMETERS</span></span>

### <span data-ttu-id="eb17c-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="eb17c-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="eb17c-122">Anger en samling med Programgateway-dataport-referenser som den här nätverks gränssnitts-IP-konfigurationen tillhör.</span><span class="sxs-lookup"><span data-stu-id="eb17c-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="eb17c-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="eb17c-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="eb17c-124">Anger en samling med Programgateway-dataport-referenser som den här nätverks gränssnitts-IP-konfigurationen tillhör.</span><span class="sxs-lookup"><span data-stu-id="eb17c-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="eb17c-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="eb17c-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="eb17c-126">Anger en samling med program säkerhets grupp referenser som denna IP-konfiguration för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="eb17c-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="eb17c-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="eb17c-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="eb17c-128">Anger en samling med program säkerhets grupp referenser som denna IP-konfiguration för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="eb17c-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="eb17c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb17c-129">-DefaultProfile</span></span>
<span data-ttu-id="eb17c-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eb17c-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb17c-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="eb17c-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="eb17c-132">Anger en samling Server grupp referenser för belastnings utjämning som den här IP-konfigurationen för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="eb17c-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="eb17c-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="eb17c-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="eb17c-134">Anger en samling Server grupp referenser för belastnings utjämning som den här IP-konfigurationen för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="eb17c-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="eb17c-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="eb17c-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="eb17c-136">Anger en samling regel referenser för inkommande nätverks adresser (NAT) som den här nätverks gränssnitts-IP-konfigurationen tillhör.</span><span class="sxs-lookup"><span data-stu-id="eb17c-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="eb17c-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="eb17c-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="eb17c-138">Anger en mängd inkommande NAT-regler för belastnings utjämning som den här IP-konfigurationen för nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="eb17c-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="eb17c-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb17c-139">-Name</span></span>
<span data-ttu-id="eb17c-140">Anger namnet på den nätverks-IP-konfiguration som cmdleten ställer in.</span><span class="sxs-lookup"><span data-stu-id="eb17c-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="eb17c-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="eb17c-141">-NetworkInterface</span></span>
<span data-ttu-id="eb17c-142">Anger ett **NetworkInterface** -objekt.</span><span class="sxs-lookup"><span data-stu-id="eb17c-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="eb17c-143">Denna cmdlet lägger till en IP-konfiguration för nätverks gränssnitt till det objekt som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="eb17c-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="eb17c-144">-Primär</span><span class="sxs-lookup"><span data-stu-id="eb17c-144">-Primary</span></span>
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

### <span data-ttu-id="eb17c-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="eb17c-145">-PrivateIpAddress</span></span>
<span data-ttu-id="eb17c-146">Anger den statiska IP-adressen för nätverks gränssnittets IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="eb17c-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="eb17c-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="eb17c-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="eb17c-148">Anger IP-adressen för en IP-konfiguration för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="eb17c-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="eb17c-149">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="eb17c-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eb17c-150">IPv4</span><span class="sxs-lookup"><span data-stu-id="eb17c-150">IPv4</span></span>
- <span data-ttu-id="eb17c-151">-</span><span class="sxs-lookup"><span data-stu-id="eb17c-151">IPv6</span></span>

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

### <span data-ttu-id="eb17c-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="eb17c-152">-PublicIpAddress</span></span>
<span data-ttu-id="eb17c-153">Anger ett **PublicIPAddress** -objekt.</span><span class="sxs-lookup"><span data-stu-id="eb17c-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="eb17c-154">Denna cmdlet skapar en referens till en offentlig IP-adress som ska kopplas till den här IP-konfigurationen för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="eb17c-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="eb17c-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="eb17c-155">-PublicIpAddressId</span></span>
<span data-ttu-id="eb17c-156">Denna cmdlet skapar en referens till en offentlig IP-adress som ska kopplas till den här IP-konfigurationen för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="eb17c-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="eb17c-157">-Undernät</span><span class="sxs-lookup"><span data-stu-id="eb17c-157">-Subnet</span></span>
<span data-ttu-id="eb17c-158">Anger ett **under näts** objekt.</span><span class="sxs-lookup"><span data-stu-id="eb17c-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="eb17c-159">Denna cmdlet skapar en referens till ett undernät där nätverks gränssnittets IP-konfiguration skapas.</span><span class="sxs-lookup"><span data-stu-id="eb17c-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="eb17c-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="eb17c-160">-SubnetId</span></span>
<span data-ttu-id="eb17c-161">Denna cmdlet skapar en referens till ett undernät där nätverks gränssnittets IP-konfiguration skapas.</span><span class="sxs-lookup"><span data-stu-id="eb17c-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="eb17c-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb17c-162">CommonParameters</span></span>
<span data-ttu-id="eb17c-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb17c-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb17c-164">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb17c-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb17c-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb17c-165">INPUTS</span></span>

### <span data-ttu-id="eb17c-166">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="eb17c-166">PSNetworkInterface</span></span>
<span data-ttu-id="eb17c-167">Parametern ' NetworkInterface ' godkänner värdet av typen ' PSNetworkInterface ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="eb17c-167">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="eb17c-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb17c-168">OUTPUTS</span></span>

### <span data-ttu-id="eb17c-169">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="eb17c-169">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="eb17c-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb17c-170">NOTES</span></span>
* <span data-ttu-id="eb17c-171">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="eb17c-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="eb17c-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb17c-172">RELATED LINKS</span></span>

[<span data-ttu-id="eb17c-173">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="eb17c-173">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="eb17c-174">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="eb17c-174">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="eb17c-175">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="eb17c-175">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="eb17c-176">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="eb17c-176">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)


