---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: feefe02c5056556d360a54819ea429cd39b84b62
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089862"
---
# <span data-ttu-id="24d98-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="24d98-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="24d98-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24d98-102">SYNOPSIS</span></span>
<span data-ttu-id="24d98-103">Skapar ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="24d98-103">Creates a network interface.</span></span>

## <span data-ttu-id="24d98-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24d98-104">SYNTAX</span></span>

### <span data-ttu-id="24d98-105">SetByIpConfigurationResource (standard)</span><span class="sxs-lookup"><span data-stu-id="24d98-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24d98-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="24d98-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24d98-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="24d98-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24d98-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="24d98-108">SetByResource</span></span>
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

## <span data-ttu-id="24d98-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24d98-109">DESCRIPTION</span></span>
<span data-ttu-id="24d98-110">Cmdleten **New-AzNetworkInterface** skapar ett Azure-nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="24d98-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="24d98-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24d98-111">EXAMPLES</span></span>

### <span data-ttu-id="24d98-112">Exempel 1: skapa ett Azure nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="24d98-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="24d98-113">Det här kommandot skapar ett nätverks gränssnitt med namnet NetworkInterface001 med en dynamiskt tilldelad privat IP-adress från Subnet1 i det virtuella nätverket med namnet VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="24d98-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="24d98-114">Kommandot tilldelar också två DNS-servrar till nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="24d98-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="24d98-115">Den underordnade resursen IPConfiguration skapas automatiskt med namnet IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="24d98-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="24d98-116">Exempel 2: skapa ett Azure nätverks gränssnitt med ett IP-konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="24d98-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="24d98-117">I det här exemplet skapas ett nytt nätverks gränssnitt med ett IP-konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="24d98-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="24d98-118">IP-konfigurationsobjektet anger en statisk privat IPv4-adress.</span><span class="sxs-lookup"><span data-stu-id="24d98-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="24d98-119">Det första kommandot hämtar ett befintligt virtuellt nätverk som används för att tilldela under nätet i det andra kommandot.</span><span class="sxs-lookup"><span data-stu-id="24d98-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="24d98-120">Det andra kommandot skapar en IP-konfiguration för ett nätverks gränssnitt med namnet IPConfig1 och lagrar konfigurationen i variabeln som heter $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="24d98-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="24d98-121">Det tredje kommandot skapar ett nätverks gränssnitt med namnet NetworkInterface1 som använder IP-konfigurationen för nätverks gränssnittet som lagras i variabeln som heter $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="24d98-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="24d98-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24d98-122">PARAMETERS</span></span>

### <span data-ttu-id="24d98-123">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="24d98-123">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="24d98-124">Anger ett **ApplicationGatewayBackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="24d98-124">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="24d98-125">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="24d98-125">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="24d98-126">Anger ID för ett **ApplicationGatewayBackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="24d98-126">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="24d98-127">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="24d98-127">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="24d98-128">Anger en samling med program säkerhets grupp referenser som nätverks gränssnittets IP-konfiguration ska tillhöra.</span><span class="sxs-lookup"><span data-stu-id="24d98-128">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="24d98-129">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="24d98-129">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="24d98-130">Anger en samling med program säkerhets grupp referenser som nätverks gränssnittets IP-konfiguration ska tillhöra.</span><span class="sxs-lookup"><span data-stu-id="24d98-130">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="24d98-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24d98-131">-AsJob</span></span>
<span data-ttu-id="24d98-132">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="24d98-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24d98-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d98-133">-DefaultProfile</span></span>
<span data-ttu-id="24d98-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="24d98-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24d98-135">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="24d98-135">-DnsServer</span></span>
<span data-ttu-id="24d98-136">Anger DNS-server för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="24d98-136">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="24d98-137">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="24d98-137">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="24d98-138">Aktiverar snabbare nätverk.</span><span class="sxs-lookup"><span data-stu-id="24d98-138">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="24d98-139">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="24d98-139">-EnableIPForwarding</span></span>
<span data-ttu-id="24d98-140">Anger att denna cmdlet aktiverar IP-vidarekoppling för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="24d98-140">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="24d98-141">Med IP-vidarebefordring kan en virtuell dator ta emot trafik adresserade till andra destinationer.</span><span class="sxs-lookup"><span data-stu-id="24d98-141">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="24d98-142">-Force</span><span class="sxs-lookup"><span data-stu-id="24d98-142">-Force</span></span>
<span data-ttu-id="24d98-143">Tvingar skapandet av nätverks gränssnittet även om det finns ett nätverks gränssnitt med samma namn.</span><span class="sxs-lookup"><span data-stu-id="24d98-143">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="24d98-144">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="24d98-144">-InternalDnsNameLabel</span></span>
<span data-ttu-id="24d98-145">Anger den interna DNS-etiketten för det nya nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="24d98-145">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="24d98-146">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="24d98-146">-IpConfiguration</span></span>
<span data-ttu-id="24d98-147">Anger den IP-konfiguration som denna cmdlet använder för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="24d98-147">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="24d98-148">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="24d98-148">-IpConfigurationName</span></span>
<span data-ttu-id="24d98-149">Anger namnet på en IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="24d98-149">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="24d98-150">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="24d98-150">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="24d98-151">Anger ett **BackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="24d98-151">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="24d98-152">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="24d98-152">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="24d98-153">Anger ID för ett **BackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="24d98-153">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="24d98-154">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="24d98-154">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="24d98-155">Anger en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="24d98-155">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="24d98-156">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="24d98-156">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="24d98-157">Anger ID för en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="24d98-157">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="24d98-158">-Plats</span><span class="sxs-lookup"><span data-stu-id="24d98-158">-Location</span></span>
<span data-ttu-id="24d98-159">Anger region för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="24d98-159">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="24d98-160">-Namn</span><span class="sxs-lookup"><span data-stu-id="24d98-160">-Name</span></span>
<span data-ttu-id="24d98-161">Anger namnet på det nätverks gränssnitt som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="24d98-161">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="24d98-162">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="24d98-162">-NetworkSecurityGroup</span></span>
<span data-ttu-id="24d98-163">Anger ett **NetworkSecurityGroup** -objekt.</span><span class="sxs-lookup"><span data-stu-id="24d98-163">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="24d98-164">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="24d98-164">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="24d98-165">Anger ID för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="24d98-165">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="24d98-166">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="24d98-166">-PrivateIpAddress</span></span>
<span data-ttu-id="24d98-167">Anger en statisk IPv4-IP-adress att tilldela det här nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="24d98-167">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="24d98-168">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="24d98-168">-PublicIpAddress</span></span>
<span data-ttu-id="24d98-169">Anger ett **PublicIPAddress** -objekt som ska kopplas till ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="24d98-169">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="24d98-170">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="24d98-170">-PublicIpAddressId</span></span>
<span data-ttu-id="24d98-171">Anger ID för ett **PublicIPAddress** -objekt som ska kopplas till ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="24d98-171">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="24d98-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24d98-172">-ResourceGroupName</span></span>
<span data-ttu-id="24d98-173">Anger namnet på en resurs grupp som nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="24d98-173">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="24d98-174">-Undernät</span><span class="sxs-lookup"><span data-stu-id="24d98-174">-Subnet</span></span>
<span data-ttu-id="24d98-175">Anger ett **under näts** objekt.</span><span class="sxs-lookup"><span data-stu-id="24d98-175">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="24d98-176">Denna cmdlet skapar ett nätverks gränssnitt för det undernät som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="24d98-176">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="24d98-177">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="24d98-177">-SubnetId</span></span>
<span data-ttu-id="24d98-178">Anger ID för det undernät som du vill skapa ett nätverks gränssnitt för.</span><span class="sxs-lookup"><span data-stu-id="24d98-178">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="24d98-179">-Tagg</span><span class="sxs-lookup"><span data-stu-id="24d98-179">-Tag</span></span>
<span data-ttu-id="24d98-180">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="24d98-180">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="24d98-181">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="24d98-181">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="24d98-182">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="24d98-182">-Confirm</span></span>
<span data-ttu-id="24d98-183">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="24d98-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24d98-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24d98-184">-WhatIf</span></span>
<span data-ttu-id="24d98-185">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="24d98-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24d98-186">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="24d98-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24d98-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d98-187">CommonParameters</span></span>
<span data-ttu-id="24d98-188">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24d98-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d98-189">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24d98-189">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d98-190">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24d98-190">INPUTS</span></span>

### <span data-ttu-id="24d98-191">System. String</span><span class="sxs-lookup"><span data-stu-id="24d98-191">System.String</span></span>

### <span data-ttu-id="24d98-192">Microsoft. Azure. commands. Network. Models. PSNetworkInterfaceIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="24d98-192">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="24d98-193">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="24d98-193">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="24d98-194">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="24d98-194">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="24d98-195">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="24d98-195">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="24d98-196">System. string []</span><span class="sxs-lookup"><span data-stu-id="24d98-196">System.String[]</span></span>

### <span data-ttu-id="24d98-197">Microsoft. Azure. commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="24d98-197">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="24d98-198">Microsoft. Azure. commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="24d98-198">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="24d98-199">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="24d98-199">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="24d98-200">Microsoft. Azure. commands. Network. Models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="24d98-200">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="24d98-201">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="24d98-201">System.Collections.Hashtable</span></span>

## <span data-ttu-id="24d98-202">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24d98-202">OUTPUTS</span></span>

### <span data-ttu-id="24d98-203">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="24d98-203">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="24d98-204">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24d98-204">NOTES</span></span>

## <span data-ttu-id="24d98-205">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24d98-205">RELATED LINKS</span></span>

[<span data-ttu-id="24d98-206">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="24d98-206">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="24d98-207">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="24d98-207">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="24d98-208">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="24d98-208">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
