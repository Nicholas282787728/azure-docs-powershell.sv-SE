---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: 63f7dc9fd60e8ef4de77790f2fb66b8143c72b8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748038"
---
# <span data-ttu-id="53cd1-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="53cd1-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="53cd1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53cd1-102">SYNOPSIS</span></span>
<span data-ttu-id="53cd1-103">Skapar ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="53cd1-103">Creates a network interface.</span></span>

## <span data-ttu-id="53cd1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53cd1-104">SYNTAX</span></span>

### <span data-ttu-id="53cd1-105">SetByIpConfigurationResource (standard)</span><span class="sxs-lookup"><span data-stu-id="53cd1-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53cd1-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="53cd1-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53cd1-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="53cd1-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53cd1-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="53cd1-108">SetByResource</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>] [-EnableIPForwarding]
 [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53cd1-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53cd1-109">DESCRIPTION</span></span>
<span data-ttu-id="53cd1-110">Cmdleten **New-AzNetworkInterface** skapar ett Azure-nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="53cd1-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="53cd1-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53cd1-111">EXAMPLES</span></span>

### <span data-ttu-id="53cd1-112">Exempel 1: skapa ett Azure nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="53cd1-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="53cd1-113">Det här kommandot skapar ett nätverks gränssnitt med namnet NetworkInterface001 med en dynamiskt tilldelad privat IP-adress från Subnet1 i det virtuella nätverket med namnet VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="53cd1-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="53cd1-114">Kommandot tilldelar också två DNS-servrar till nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="53cd1-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="53cd1-115">Den underordnade resursen IPConfiguration skapas automatiskt med namnet IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="53cd1-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="53cd1-116">Exempel 2: skapa ett Azure nätverks gränssnitt med ett IP-konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="53cd1-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="53cd1-117">I det här exemplet skapas ett nytt nätverks gränssnitt med ett IP-konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="53cd1-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="53cd1-118">IP-konfigurationsobjektet anger en statisk privat IPv4-adress.</span><span class="sxs-lookup"><span data-stu-id="53cd1-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="53cd1-119">Det första kommandot skapar en IP-konfiguration för ett nätverks gränssnitt med namnet IPConfig1 och lagrar konfigurationen i variabeln som heter $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="53cd1-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="53cd1-120">Det andra kommandot skapar ett nätverks gränssnitt med namnet NetworkInterface1 som använder IP-konfigurationen för nätverks gränssnittet som lagras i variabeln $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="53cd1-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="53cd1-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53cd1-121">PARAMETERS</span></span>

### <span data-ttu-id="53cd1-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="53cd1-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="53cd1-123">Anger ett **ApplicationGatewayBackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="53cd1-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="53cd1-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="53cd1-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="53cd1-125">Anger ID för ett **ApplicationGatewayBackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="53cd1-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="53cd1-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="53cd1-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="53cd1-127">Anger en samling med program säkerhets grupp referenser som nätverks gränssnittets IP-konfiguration ska tillhöra.</span><span class="sxs-lookup"><span data-stu-id="53cd1-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="53cd1-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="53cd1-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="53cd1-129">Anger en samling med program säkerhets grupp referenser som nätverks gränssnittets IP-konfiguration ska tillhöra.</span><span class="sxs-lookup"><span data-stu-id="53cd1-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="53cd1-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53cd1-130">-AsJob</span></span>
<span data-ttu-id="53cd1-131">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="53cd1-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53cd1-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53cd1-132">-DefaultProfile</span></span>
<span data-ttu-id="53cd1-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53cd1-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53cd1-134">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="53cd1-134">-DnsServer</span></span>
<span data-ttu-id="53cd1-135">Anger DNS-server för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="53cd1-135">Specifies the DNS server for the network interface.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53cd1-136">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="53cd1-136">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="53cd1-137">Aktiverar snabbare nätverk.</span><span class="sxs-lookup"><span data-stu-id="53cd1-137">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="53cd1-138">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="53cd1-138">-EnableIPForwarding</span></span>
<span data-ttu-id="53cd1-139">Anger att denna cmdlet aktiverar IP-vidarekoppling för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="53cd1-139">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="53cd1-140">Med IP-vidarebefordring kan en virtuell dator ta emot trafik adresserade till andra destinationer.</span><span class="sxs-lookup"><span data-stu-id="53cd1-140">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="53cd1-141">-Force</span><span class="sxs-lookup"><span data-stu-id="53cd1-141">-Force</span></span>
<span data-ttu-id="53cd1-142">Tvingar skapandet av nätverks gränssnittet även om det finns ett nätverks gränssnitt med samma namn.</span><span class="sxs-lookup"><span data-stu-id="53cd1-142">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="53cd1-143">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="53cd1-143">-InternalDnsNameLabel</span></span>
<span data-ttu-id="53cd1-144">Anger den interna DNS-etiketten för det nya nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="53cd1-144">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="53cd1-145">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="53cd1-145">-IpConfiguration</span></span>
<span data-ttu-id="53cd1-146">Anger den IP-konfiguration som denna cmdlet använder för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="53cd1-146">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]
Parameter Sets: SetByIpConfigurationResource, SetByIpConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53cd1-147">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="53cd1-147">-IpConfigurationName</span></span>
<span data-ttu-id="53cd1-148">Anger namnet på en IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="53cd1-148">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="53cd1-149">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="53cd1-149">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="53cd1-150">Anger ett **BackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="53cd1-150">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="53cd1-151">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="53cd1-151">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="53cd1-152">Anger ID för ett **BackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="53cd1-152">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="53cd1-153">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="53cd1-153">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="53cd1-154">Anger en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="53cd1-154">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="53cd1-155">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="53cd1-155">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="53cd1-156">Anger ID för en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="53cd1-156">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="53cd1-157">-Plats</span><span class="sxs-lookup"><span data-stu-id="53cd1-157">-Location</span></span>
<span data-ttu-id="53cd1-158">Anger region för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="53cd1-158">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="53cd1-159">-Namn</span><span class="sxs-lookup"><span data-stu-id="53cd1-159">-Name</span></span>
<span data-ttu-id="53cd1-160">Anger namnet på det nätverks gränssnitt som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="53cd1-160">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="53cd1-161">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="53cd1-161">-NetworkSecurityGroup</span></span>
<span data-ttu-id="53cd1-162">Anger ett **NetworkSecurityGroup** -objekt.</span><span class="sxs-lookup"><span data-stu-id="53cd1-162">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="53cd1-163">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="53cd1-163">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="53cd1-164">Anger ID för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="53cd1-164">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="53cd1-165">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="53cd1-165">-PrivateIpAddress</span></span>
<span data-ttu-id="53cd1-166">Anger en statisk IPv4-IP-adress att tilldela det här nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="53cd1-166">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="53cd1-167">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="53cd1-167">-PublicIpAddress</span></span>
<span data-ttu-id="53cd1-168">Anger ett **PublicIPAddress** -objekt som ska kopplas till ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="53cd1-168">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="53cd1-169">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="53cd1-169">-PublicIpAddressId</span></span>
<span data-ttu-id="53cd1-170">Anger ID för ett **PublicIPAddress** -objekt som ska kopplas till ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="53cd1-170">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="53cd1-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53cd1-171">-ResourceGroupName</span></span>
<span data-ttu-id="53cd1-172">Anger namnet på en resurs grupp som nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="53cd1-172">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="53cd1-173">-Undernät</span><span class="sxs-lookup"><span data-stu-id="53cd1-173">-Subnet</span></span>
<span data-ttu-id="53cd1-174">Anger ett **under näts** objekt.</span><span class="sxs-lookup"><span data-stu-id="53cd1-174">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="53cd1-175">Denna cmdlet skapar ett nätverks gränssnitt för det undernät som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="53cd1-175">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="53cd1-176">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="53cd1-176">-SubnetId</span></span>
<span data-ttu-id="53cd1-177">Anger ID för det undernät som du vill skapa ett nätverks gränssnitt för.</span><span class="sxs-lookup"><span data-stu-id="53cd1-177">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="53cd1-178">-Tagg</span><span class="sxs-lookup"><span data-stu-id="53cd1-178">-Tag</span></span>
<span data-ttu-id="53cd1-179">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="53cd1-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="53cd1-180">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="53cd1-180">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="53cd1-181">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="53cd1-181">-Confirm</span></span>
<span data-ttu-id="53cd1-182">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="53cd1-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53cd1-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53cd1-183">-WhatIf</span></span>
<span data-ttu-id="53cd1-184">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="53cd1-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53cd1-185">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="53cd1-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53cd1-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53cd1-186">CommonParameters</span></span>
<span data-ttu-id="53cd1-187">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53cd1-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53cd1-188">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53cd1-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53cd1-189">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53cd1-189">INPUTS</span></span>

### <span data-ttu-id="53cd1-190">System. String</span><span class="sxs-lookup"><span data-stu-id="53cd1-190">System.String</span></span>

### <span data-ttu-id="53cd1-191">Microsoft. Azure. commands. Network. Models. PSNetworkInterfaceIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="53cd1-191">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="53cd1-192">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="53cd1-192">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="53cd1-193">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="53cd1-193">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="53cd1-194">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="53cd1-194">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="53cd1-195">System. string []</span><span class="sxs-lookup"><span data-stu-id="53cd1-195">System.String[]</span></span>

### <span data-ttu-id="53cd1-196">Microsoft. Azure. commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="53cd1-196">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="53cd1-197">Microsoft. Azure. commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="53cd1-197">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="53cd1-198">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="53cd1-198">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="53cd1-199">Microsoft. Azure. commands. Network. Models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="53cd1-199">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="53cd1-200">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="53cd1-200">System.Collections.Hashtable</span></span>

## <span data-ttu-id="53cd1-201">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53cd1-201">OUTPUTS</span></span>

### <span data-ttu-id="53cd1-202">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="53cd1-202">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="53cd1-203">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53cd1-203">NOTES</span></span>

## <span data-ttu-id="53cd1-204">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53cd1-204">RELATED LINKS</span></span>

[<span data-ttu-id="53cd1-205">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="53cd1-205">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="53cd1-206">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="53cd1-206">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="53cd1-207">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="53cd1-207">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
