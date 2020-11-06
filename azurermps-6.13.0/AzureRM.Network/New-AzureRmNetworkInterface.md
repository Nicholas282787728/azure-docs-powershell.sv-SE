---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
ms.openlocfilehash: 90a3696b4f641f0518d08f821cab813effdbc74a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576884"
---
# <span data-ttu-id="d5690-101">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d5690-101">New-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="d5690-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d5690-102">SYNOPSIS</span></span>
<span data-ttu-id="d5690-103">Skapar ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="d5690-103">Creates a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5690-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d5690-104">SYNTAX</span></span>

### <span data-ttu-id="d5690-105">SetByIpConfigurationResource (standard)</span><span class="sxs-lookup"><span data-stu-id="d5690-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5690-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="d5690-106">SetByIpConfigurationResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-NetworkSecurityGroupId <String>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5690-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d5690-107">SetByResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5690-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d5690-108">SetByResource</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5690-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d5690-109">DESCRIPTION</span></span>
<span data-ttu-id="d5690-110">Cmdleten **New-AzureRmNetworkInterface** skapar ett Azure-nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="d5690-110">The **New-AzureRmNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="d5690-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d5690-111">EXAMPLES</span></span>

### <span data-ttu-id="d5690-112">Exempel 1: skapa ett Azure nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="d5690-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="d5690-113">Det här kommandot skapar ett nätverks gränssnitt med namnet NetworkInterface001 med en dynamiskt tilldelad privat IP-adress från Subnet1 i det virtuella nätverket med namnet VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="d5690-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="d5690-114">Kommandot tilldelar också två DNS-servrar till nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="d5690-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="d5690-115">Den underordnade resursen IPConfiguration skapas automatiskt med namnet IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="d5690-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="d5690-116">Exempel 2: skapa ett Azure nätverks gränssnitt med ett IP-konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="d5690-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzureRmNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="d5690-117">I det här exemplet skapas ett nytt nätverks gränssnitt med ett IP-konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="d5690-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="d5690-118">IP-konfigurationsobjektet anger en statisk privat IPv4-adress.</span><span class="sxs-lookup"><span data-stu-id="d5690-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="d5690-119">Det första kommandot skapar en IP-konfiguration för ett nätverks gränssnitt med namnet IPConfig1 och lagrar konfigurationen i variabeln som heter $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="d5690-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="d5690-120">Det andra kommandot skapar ett nätverks gränssnitt med namnet NetworkInterface1 som använder IP-konfigurationen för nätverks gränssnittet som lagras i variabeln $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="d5690-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="d5690-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d5690-121">PARAMETERS</span></span>

### <span data-ttu-id="d5690-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d5690-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="d5690-123">Anger ett **ApplicationGatewayBackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d5690-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="d5690-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d5690-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="d5690-125">Anger ID för ett **ApplicationGatewayBackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d5690-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="d5690-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d5690-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="d5690-127">Anger en samling med program säkerhets grupp referenser som nätverks gränssnittets IP-konfiguration ska tillhöra.</span><span class="sxs-lookup"><span data-stu-id="d5690-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="d5690-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d5690-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="d5690-129">Anger en samling med program säkerhets grupp referenser som nätverks gränssnittets IP-konfiguration ska tillhöra.</span><span class="sxs-lookup"><span data-stu-id="d5690-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="d5690-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5690-130">-AsJob</span></span>
<span data-ttu-id="d5690-131">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d5690-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5690-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5690-132">-DefaultProfile</span></span>
<span data-ttu-id="d5690-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d5690-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5690-134">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="d5690-134">-DnsServer</span></span>
<span data-ttu-id="d5690-135">Anger DNS-server för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="d5690-135">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="d5690-136">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="d5690-136">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="d5690-137">Aktiverar snabbare nätverk.</span><span class="sxs-lookup"><span data-stu-id="d5690-137">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="d5690-138">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="d5690-138">-EnableIPForwarding</span></span>
<span data-ttu-id="d5690-139">Anger att denna cmdlet aktiverar IP-vidarekoppling för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="d5690-139">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="d5690-140">Med IP-vidarebefordring kan en virtuell dator ta emot trafik adresserade till andra destinationer.</span><span class="sxs-lookup"><span data-stu-id="d5690-140">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="d5690-141">-Force</span><span class="sxs-lookup"><span data-stu-id="d5690-141">-Force</span></span>
<span data-ttu-id="d5690-142">Tvingar skapandet av nätverks gränssnittet även om det finns ett nätverks gränssnitt med samma namn.</span><span class="sxs-lookup"><span data-stu-id="d5690-142">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="d5690-143">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="d5690-143">-InternalDnsNameLabel</span></span>
<span data-ttu-id="d5690-144">Anger den interna DNS-etiketten för det nya nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="d5690-144">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="d5690-145">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5690-145">-IpConfiguration</span></span>
<span data-ttu-id="d5690-146">Anger den IP-konfiguration som denna cmdlet använder för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="d5690-146">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="d5690-147">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d5690-147">-IpConfigurationName</span></span>
<span data-ttu-id="d5690-148">Anger namnet på en IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d5690-148">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="d5690-149">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d5690-149">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="d5690-150">Anger ett **BackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d5690-150">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="d5690-151">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d5690-151">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="d5690-152">Anger ID för ett **BackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d5690-152">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="d5690-153">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="d5690-153">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="d5690-154">Anger en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="d5690-154">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="d5690-155">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="d5690-155">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="d5690-156">Anger ID för en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="d5690-156">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="d5690-157">-Plats</span><span class="sxs-lookup"><span data-stu-id="d5690-157">-Location</span></span>
<span data-ttu-id="d5690-158">Anger region för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="d5690-158">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="d5690-159">-Namn</span><span class="sxs-lookup"><span data-stu-id="d5690-159">-Name</span></span>
<span data-ttu-id="d5690-160">Anger namnet på det nätverks gränssnitt som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="d5690-160">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="d5690-161">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d5690-161">-NetworkSecurityGroup</span></span>
<span data-ttu-id="d5690-162">Anger ett **NetworkSecurityGroup** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d5690-162">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="d5690-163">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d5690-163">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="d5690-164">Anger ID för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="d5690-164">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="d5690-165">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="d5690-165">-PrivateIpAddress</span></span>
<span data-ttu-id="d5690-166">Anger en statisk IPv4-IP-adress att tilldela det här nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="d5690-166">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="d5690-167">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d5690-167">-PublicIpAddress</span></span>
<span data-ttu-id="d5690-168">Anger ett **PublicIPAddress** -objekt som ska kopplas till ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="d5690-168">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="d5690-169">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="d5690-169">-PublicIpAddressId</span></span>
<span data-ttu-id="d5690-170">Anger ID för ett **PublicIPAddress** -objekt som ska kopplas till ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="d5690-170">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="d5690-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5690-171">-ResourceGroupName</span></span>
<span data-ttu-id="d5690-172">Anger namnet på en resurs grupp som nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="d5690-172">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="d5690-173">-Undernät</span><span class="sxs-lookup"><span data-stu-id="d5690-173">-Subnet</span></span>
<span data-ttu-id="d5690-174">Anger ett **under näts** objekt.</span><span class="sxs-lookup"><span data-stu-id="d5690-174">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="d5690-175">Denna cmdlet skapar ett nätverks gränssnitt för det undernät som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="d5690-175">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="d5690-176">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d5690-176">-SubnetId</span></span>
<span data-ttu-id="d5690-177">Anger ID för det undernät som du vill skapa ett nätverks gränssnitt för.</span><span class="sxs-lookup"><span data-stu-id="d5690-177">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="d5690-178">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d5690-178">-Tag</span></span>
<span data-ttu-id="d5690-179">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d5690-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d5690-180">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="d5690-180">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d5690-181">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d5690-181">-Confirm</span></span>
<span data-ttu-id="d5690-182">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d5690-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5690-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5690-183">-WhatIf</span></span>
<span data-ttu-id="d5690-184">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d5690-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5690-185">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d5690-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5690-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5690-186">CommonParameters</span></span>
<span data-ttu-id="d5690-187">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5690-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5690-188">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5690-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5690-189">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d5690-189">INPUTS</span></span>

### <span data-ttu-id="d5690-190">System. String</span><span class="sxs-lookup"><span data-stu-id="d5690-190">System.String</span></span>

### <span data-ttu-id="d5690-191">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSNetworkInterfaceIPConfiguration, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d5690-191">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d5690-192">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="d5690-192">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="d5690-193">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d5690-193">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="d5690-194">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d5690-194">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="d5690-195">System. Collections. Generic. list ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d5690-195">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d5690-196">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSBackendAddressPool, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d5690-196">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d5690-197">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSInboundNatRule, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d5690-197">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d5690-198">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewayBackendAddressPool, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d5690-198">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d5690-199">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationSecurityGroup, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d5690-199">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d5690-200">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="d5690-200">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d5690-201">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d5690-201">OUTPUTS</span></span>

### <span data-ttu-id="d5690-202">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d5690-202">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="d5690-203">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d5690-203">NOTES</span></span>

## <span data-ttu-id="d5690-204">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d5690-204">RELATED LINKS</span></span>

[<span data-ttu-id="d5690-205">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d5690-205">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="d5690-206">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d5690-206">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="d5690-207">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d5690-207">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)
