---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
ms.openlocfilehash: 75e16da63a5348b47a5b67042a2fb1e2078206c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756913"
---
# <span data-ttu-id="809f6-101">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="809f6-101">New-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="809f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="809f6-102">SYNOPSIS</span></span>
<span data-ttu-id="809f6-103">Skapar ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="809f6-103">Creates a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="809f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="809f6-104">SYNTAX</span></span>

### <span data-ttu-id="809f6-105">SetByIpConfigurationResource (standard)</span><span class="sxs-lookup"><span data-stu-id="809f6-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="809f6-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="809f6-106">SetByIpConfigurationResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-NetworkSecurityGroupId <String>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="809f6-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="809f6-107">SetByResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="809f6-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="809f6-108">SetByResource</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="809f6-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="809f6-109">DESCRIPTION</span></span>
<span data-ttu-id="809f6-110">Cmdleten **New-AzureRmNetworkInterface** skapar ett Azure-nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="809f6-110">The **New-AzureRmNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="809f6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="809f6-111">EXAMPLES</span></span>

### <span data-ttu-id="809f6-112">Exempel 1: skapa ett Azure nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="809f6-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="809f6-113">Det här kommandot skapar ett nätverks gränssnitt med namnet NetworkInterface001 med en dynamiskt tilldelad privat IP-adress från Subnet1 i det virtuella nätverket med namnet VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="809f6-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="809f6-114">Kommandot tilldelar också två DNS-servrar till nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="809f6-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="809f6-115">Den underordnade resursen IPConfiguration skapas automatiskt med namnet IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="809f6-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="809f6-116">Exempel 2: skapa ett Azure nätverks gränssnitt med ett IP-konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="809f6-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzureRmNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="809f6-117">I det här exemplet skapas ett nytt nätverks gränssnitt med ett IP-konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="809f6-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="809f6-118">IP-konfigurationsobjektet anger en statisk privat IPv4-adress.</span><span class="sxs-lookup"><span data-stu-id="809f6-118">The IP configuration object specifies a static private IPv4 address.</span></span>

<span data-ttu-id="809f6-119">Det första kommandot skapar en IP-konfiguration för ett nätverks gränssnitt med namnet IPConfig1 och lagrar konfigurationen i variabeln som heter $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="809f6-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>

<span data-ttu-id="809f6-120">Det andra kommandot skapar ett nätverks gränssnitt med namnet NetworkInterface1 som använder IP-konfigurationen för nätverks gränssnittet som lagras i variabeln $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="809f6-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="809f6-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="809f6-121">PARAMETERS</span></span>

### <span data-ttu-id="809f6-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="809f6-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="809f6-123">Anger ett **ApplicationGatewayBackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="809f6-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="809f6-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="809f6-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="809f6-125">Anger ID för ett **ApplicationGatewayBackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="809f6-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="809f6-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="809f6-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="809f6-127">Anger en samling med program säkerhets grupp referenser som nätverks gränssnittets IP-konfiguration ska tillhöra.</span><span class="sxs-lookup"><span data-stu-id="809f6-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="809f6-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="809f6-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="809f6-129">Anger en samling med program säkerhets grupp referenser som nätverks gränssnittets IP-konfiguration ska tillhöra.</span><span class="sxs-lookup"><span data-stu-id="809f6-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="809f6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="809f6-130">-DefaultProfile</span></span>
<span data-ttu-id="809f6-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="809f6-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="809f6-132">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="809f6-132">-DnsServer</span></span>
<span data-ttu-id="809f6-133">Anger DNS-server för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="809f6-133">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="809f6-134">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="809f6-134">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="809f6-135">Aktiverar snabbare nätverk.</span><span class="sxs-lookup"><span data-stu-id="809f6-135">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="809f6-136">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="809f6-136">-EnableIPForwarding</span></span>
<span data-ttu-id="809f6-137">Anger att denna cmdlet aktiverar IP-vidarekoppling för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="809f6-137">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="809f6-138">Med IP-vidarebefordring kan en virtuell dator ta emot trafik adresserade till andra destinationer.</span><span class="sxs-lookup"><span data-stu-id="809f6-138">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="809f6-139">-Force</span><span class="sxs-lookup"><span data-stu-id="809f6-139">-Force</span></span>
<span data-ttu-id="809f6-140">Tvingar skapandet av nätverks gränssnittet även om det finns ett nätverks gränssnitt med samma namn.</span><span class="sxs-lookup"><span data-stu-id="809f6-140">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="809f6-141">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="809f6-141">-InternalDnsNameLabel</span></span>
<span data-ttu-id="809f6-142">Anger den interna DNS-etiketten för det nya nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="809f6-142">Specifies the internal DNS name label for the new network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="809f6-143">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="809f6-143">-IpConfiguration</span></span>
<span data-ttu-id="809f6-144">Anger den IP-konfiguration som denna cmdlet använder för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="809f6-144">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]
Parameter Sets: SetByIpConfigurationResource, SetByIpConfigurationResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="809f6-145">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="809f6-145">-IpConfigurationName</span></span>
<span data-ttu-id="809f6-146">Anger namnet på en IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="809f6-146">Specifies the name of an IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="809f6-147">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="809f6-147">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="809f6-148">Anger ett **BackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="809f6-148">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="809f6-149">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="809f6-149">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="809f6-150">Anger ID för ett **BackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="809f6-150">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="809f6-151">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="809f6-151">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="809f6-152">Anger en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="809f6-152">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="809f6-153">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="809f6-153">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="809f6-154">Anger ID för en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="809f6-154">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="809f6-155">-Plats</span><span class="sxs-lookup"><span data-stu-id="809f6-155">-Location</span></span>
<span data-ttu-id="809f6-156">Anger region för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="809f6-156">Specifies the region for a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="809f6-157">-Namn</span><span class="sxs-lookup"><span data-stu-id="809f6-157">-Name</span></span>
<span data-ttu-id="809f6-158">Anger namnet på det nätverks gränssnitt som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="809f6-158">Specifies the name of the network interface to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="809f6-159">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="809f6-159">-NetworkSecurityGroup</span></span>
<span data-ttu-id="809f6-160">Anger ett **NetworkSecurityGroup** -objekt.</span><span class="sxs-lookup"><span data-stu-id="809f6-160">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByIpConfigurationResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="809f6-161">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="809f6-161">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="809f6-162">Anger ID för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="809f6-162">Specifies the ID of a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIpConfigurationResourceId, SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="809f6-163">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="809f6-163">-PrivateIpAddress</span></span>
<span data-ttu-id="809f6-164">Anger en statisk IPv4-IP-adress att tilldela det här nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="809f6-164">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="809f6-165">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="809f6-165">-PublicIpAddress</span></span>
<span data-ttu-id="809f6-166">Anger ett **PublicIPAddress** -objekt som ska kopplas till ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="809f6-166">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="809f6-167">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="809f6-167">-PublicIpAddressId</span></span>
<span data-ttu-id="809f6-168">Anger ID för ett **PublicIPAddress** -objekt som ska kopplas till ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="809f6-168">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="809f6-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="809f6-169">-ResourceGroupName</span></span>
<span data-ttu-id="809f6-170">Anger namnet på en resurs grupp som nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="809f6-170">Specifies the name of a resource group that the network interface belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="809f6-171">-Undernät</span><span class="sxs-lookup"><span data-stu-id="809f6-171">-Subnet</span></span>
<span data-ttu-id="809f6-172">Anger ett **under näts** objekt.</span><span class="sxs-lookup"><span data-stu-id="809f6-172">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="809f6-173">Denna cmdlet skapar ett nätverks gränssnitt för det undernät som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="809f6-173">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="809f6-174">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="809f6-174">-SubnetId</span></span>
<span data-ttu-id="809f6-175">Anger ID för det undernät som du vill skapa ett nätverks gränssnitt för.</span><span class="sxs-lookup"><span data-stu-id="809f6-175">Specifies the ID of the subnet for which to create a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="809f6-176">-Tagg</span><span class="sxs-lookup"><span data-stu-id="809f6-176">-Tag</span></span>
<span data-ttu-id="809f6-177">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="809f6-177">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="809f6-178">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="809f6-178">For example:</span></span>

<span data-ttu-id="809f6-179">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="809f6-179">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="809f6-180">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="809f6-180">-Confirm</span></span>
<span data-ttu-id="809f6-181">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="809f6-181">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="809f6-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="809f6-182">-WhatIf</span></span>
<span data-ttu-id="809f6-183">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="809f6-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="809f6-184">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="809f6-184">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="809f6-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="809f6-185">CommonParameters</span></span>
<span data-ttu-id="809f6-186">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="809f6-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="809f6-187">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="809f6-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="809f6-188">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="809f6-188">INPUTS</span></span>

## <span data-ttu-id="809f6-189">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="809f6-189">OUTPUTS</span></span>

### <span data-ttu-id="809f6-190">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="809f6-190">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="809f6-191">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="809f6-191">NOTES</span></span>

## <span data-ttu-id="809f6-192">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="809f6-192">RELATED LINKS</span></span>

[<span data-ttu-id="809f6-193">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="809f6-193">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="809f6-194">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="809f6-194">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="809f6-195">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="809f6-195">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)
