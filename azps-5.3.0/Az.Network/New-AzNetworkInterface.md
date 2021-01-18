---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: 23d0b2eacb5e4053cbed2c08101e225d861311de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523863"
---
# <span data-ttu-id="79b2e-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="79b2e-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="79b2e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79b2e-102">SYNOPSIS</span></span>
<span data-ttu-id="79b2e-103">Skapar ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="79b2e-103">Creates a network interface.</span></span>

## <span data-ttu-id="79b2e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79b2e-104">SYNTAX</span></span>

### <span data-ttu-id="79b2e-105">SetByIpConfigurationResource (standard)</span><span class="sxs-lookup"><span data-stu-id="79b2e-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79b2e-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="79b2e-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79b2e-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="79b2e-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79b2e-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="79b2e-108">SetByResource</span></span>
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

## <span data-ttu-id="79b2e-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79b2e-109">DESCRIPTION</span></span>
<span data-ttu-id="79b2e-110">Cmdleten **New-AzNetworkInterface** skapar ett Azure-nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="79b2e-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="79b2e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79b2e-111">EXAMPLES</span></span>

### <span data-ttu-id="79b2e-112">Exempel 1: skapa ett Azure nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="79b2e-112">Example 1: Create an Azure network interface</span></span>
```powershell
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="79b2e-113">Det här kommandot skapar ett nätverks gränssnitt med namnet NetworkInterface001 med en dynamiskt tilldelad privat IP-adress från Subnet1 i det virtuella nätverket med namnet VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="79b2e-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="79b2e-114">Kommandot tilldelar också två DNS-servrar till nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="79b2e-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="79b2e-115">Den underordnade resursen IPConfiguration skapas automatiskt med namnet IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="79b2e-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="79b2e-116">Exempel 2: skapa ett Azure nätverks gränssnitt med ett IP-konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="79b2e-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```powershell
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="79b2e-117">I det här exemplet skapas ett nytt nätverks gränssnitt med ett IP-konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="79b2e-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="79b2e-118">IP-konfigurationsobjektet anger en statisk privat IPv4-adress.</span><span class="sxs-lookup"><span data-stu-id="79b2e-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="79b2e-119">Det första kommandot hämtar ett befintligt virtuellt nätverk som används för att tilldela under nätet i det andra kommandot.</span><span class="sxs-lookup"><span data-stu-id="79b2e-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="79b2e-120">Det andra kommandot skapar en IP-konfiguration för ett nätverks gränssnitt med namnet IPConfig1 och lagrar konfigurationen i variabeln som heter $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="79b2e-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="79b2e-121">Det tredje kommandot skapar ett nätverks gränssnitt med namnet NetworkInterface1 som använder IP-konfigurationen för nätverks gränssnittet som lagras i variabeln som heter $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="79b2e-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

### <span data-ttu-id="79b2e-122">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="79b2e-122">Example 3</span></span>

<span data-ttu-id="79b2e-123">Skapar ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="79b2e-123">Creates a network interface.</span></span> <span data-ttu-id="79b2e-124">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="79b2e-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzNetworkInterface -Location 'West US' -Name 'NetworkInterface1' -PrivateIpAddress '10.0.1.10' -ResourceGroupName 'ResourceGroup1' -SubnetId '/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1'
```

## <span data-ttu-id="79b2e-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79b2e-125">PARAMETERS</span></span>

### <span data-ttu-id="79b2e-126">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="79b2e-126">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="79b2e-127">Anger ett **ApplicationGatewayBackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="79b2e-127">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="79b2e-128">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="79b2e-128">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="79b2e-129">Anger ID för ett **ApplicationGatewayBackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="79b2e-129">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="79b2e-130">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="79b2e-130">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="79b2e-131">Anger en samling med program säkerhets grupp referenser som nätverks gränssnittets IP-konfiguration ska tillhöra.</span><span class="sxs-lookup"><span data-stu-id="79b2e-131">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="79b2e-132">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="79b2e-132">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="79b2e-133">Anger en samling med program säkerhets grupp referenser som nätverks gränssnittets IP-konfiguration ska tillhöra.</span><span class="sxs-lookup"><span data-stu-id="79b2e-133">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="79b2e-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79b2e-134">-AsJob</span></span>
<span data-ttu-id="79b2e-135">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="79b2e-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79b2e-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79b2e-136">-DefaultProfile</span></span>
<span data-ttu-id="79b2e-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79b2e-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79b2e-138">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="79b2e-138">-DnsServer</span></span>
<span data-ttu-id="79b2e-139">Anger DNS-server för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="79b2e-139">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="79b2e-140">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="79b2e-140">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="79b2e-141">Aktiverar snabbare nätverk.</span><span class="sxs-lookup"><span data-stu-id="79b2e-141">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="79b2e-142">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="79b2e-142">-EnableIPForwarding</span></span>
<span data-ttu-id="79b2e-143">Anger att denna cmdlet aktiverar IP-vidarekoppling för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="79b2e-143">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="79b2e-144">Med IP-vidarebefordring kan en virtuell dator ta emot trafik adresserade till andra destinationer.</span><span class="sxs-lookup"><span data-stu-id="79b2e-144">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="79b2e-145">-Force</span><span class="sxs-lookup"><span data-stu-id="79b2e-145">-Force</span></span>
<span data-ttu-id="79b2e-146">Tvingar skapandet av nätverks gränssnittet även om det finns ett nätverks gränssnitt med samma namn.</span><span class="sxs-lookup"><span data-stu-id="79b2e-146">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="79b2e-147">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="79b2e-147">-InternalDnsNameLabel</span></span>
<span data-ttu-id="79b2e-148">Anger den interna DNS-etiketten för det nya nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="79b2e-148">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="79b2e-149">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="79b2e-149">-IpConfiguration</span></span>
<span data-ttu-id="79b2e-150">Anger den IP-konfiguration som denna cmdlet använder för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="79b2e-150">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="79b2e-151">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="79b2e-151">-IpConfigurationName</span></span>
<span data-ttu-id="79b2e-152">Anger namnet på en IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="79b2e-152">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="79b2e-153">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="79b2e-153">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="79b2e-154">Anger ett **BackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="79b2e-154">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="79b2e-155">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="79b2e-155">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="79b2e-156">Anger ID för ett **BackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="79b2e-156">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="79b2e-157">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="79b2e-157">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="79b2e-158">Anger en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="79b2e-158">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="79b2e-159">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="79b2e-159">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="79b2e-160">Anger ID för en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="79b2e-160">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="79b2e-161">-Plats</span><span class="sxs-lookup"><span data-stu-id="79b2e-161">-Location</span></span>
<span data-ttu-id="79b2e-162">Anger region för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="79b2e-162">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="79b2e-163">-Namn</span><span class="sxs-lookup"><span data-stu-id="79b2e-163">-Name</span></span>
<span data-ttu-id="79b2e-164">Anger namnet på det nätverks gränssnitt som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="79b2e-164">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="79b2e-165">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="79b2e-165">-NetworkSecurityGroup</span></span>
<span data-ttu-id="79b2e-166">Anger ett **NetworkSecurityGroup** -objekt.</span><span class="sxs-lookup"><span data-stu-id="79b2e-166">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="79b2e-167">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="79b2e-167">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="79b2e-168">Anger ID för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="79b2e-168">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="79b2e-169">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="79b2e-169">-PrivateIpAddress</span></span>
<span data-ttu-id="79b2e-170">Anger en statisk IPv4-IP-adress att tilldela det här nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="79b2e-170">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="79b2e-171">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="79b2e-171">-PublicIpAddress</span></span>
<span data-ttu-id="79b2e-172">Anger ett **PublicIPAddress** -objekt som ska kopplas till ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="79b2e-172">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="79b2e-173">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="79b2e-173">-PublicIpAddressId</span></span>
<span data-ttu-id="79b2e-174">Anger ID för ett **PublicIPAddress** -objekt som ska kopplas till ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="79b2e-174">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="79b2e-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79b2e-175">-ResourceGroupName</span></span>
<span data-ttu-id="79b2e-176">Anger namnet på en resurs grupp som nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="79b2e-176">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="79b2e-177">-Undernät</span><span class="sxs-lookup"><span data-stu-id="79b2e-177">-Subnet</span></span>
<span data-ttu-id="79b2e-178">Anger ett **under näts** objekt.</span><span class="sxs-lookup"><span data-stu-id="79b2e-178">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="79b2e-179">Denna cmdlet skapar ett nätverks gränssnitt för det undernät som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="79b2e-179">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="79b2e-180">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="79b2e-180">-SubnetId</span></span>
<span data-ttu-id="79b2e-181">Anger ID för det undernät som du vill skapa ett nätverks gränssnitt för.</span><span class="sxs-lookup"><span data-stu-id="79b2e-181">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="79b2e-182">-Tagg</span><span class="sxs-lookup"><span data-stu-id="79b2e-182">-Tag</span></span>
<span data-ttu-id="79b2e-183">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="79b2e-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="79b2e-184">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="79b2e-184">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="79b2e-185">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="79b2e-185">-Confirm</span></span>
<span data-ttu-id="79b2e-186">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="79b2e-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79b2e-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79b2e-187">-WhatIf</span></span>
<span data-ttu-id="79b2e-188">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="79b2e-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79b2e-189">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="79b2e-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79b2e-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b2e-190">CommonParameters</span></span>
<span data-ttu-id="79b2e-191">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79b2e-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b2e-192">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79b2e-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b2e-193">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79b2e-193">INPUTS</span></span>

### <span data-ttu-id="79b2e-194">System. String</span><span class="sxs-lookup"><span data-stu-id="79b2e-194">System.String</span></span>

### <span data-ttu-id="79b2e-195">Microsoft. Azure. commands. Network. Models. PSNetworkInterfaceIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="79b2e-195">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="79b2e-196">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="79b2e-196">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="79b2e-197">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="79b2e-197">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="79b2e-198">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="79b2e-198">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="79b2e-199">System. string []</span><span class="sxs-lookup"><span data-stu-id="79b2e-199">System.String[]</span></span>

### <span data-ttu-id="79b2e-200">Microsoft. Azure. commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="79b2e-200">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="79b2e-201">Microsoft. Azure. commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="79b2e-201">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="79b2e-202">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="79b2e-202">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="79b2e-203">Microsoft. Azure. commands. Network. Models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="79b2e-203">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="79b2e-204">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="79b2e-204">System.Collections.Hashtable</span></span>

## <span data-ttu-id="79b2e-205">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79b2e-205">OUTPUTS</span></span>

### <span data-ttu-id="79b2e-206">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="79b2e-206">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="79b2e-207">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79b2e-207">NOTES</span></span>

## <span data-ttu-id="79b2e-208">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79b2e-208">RELATED LINKS</span></span>

[<span data-ttu-id="79b2e-209">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="79b2e-209">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="79b2e-210">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="79b2e-210">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="79b2e-211">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="79b2e-211">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
