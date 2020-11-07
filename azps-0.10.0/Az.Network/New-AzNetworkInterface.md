---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: a4a40f67eef901cd1e93ac004fa01a3224ab222e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922119"
---
# <span data-ttu-id="3c7a9-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3c7a9-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="3c7a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c7a9-102">SYNOPSIS</span></span>
<span data-ttu-id="3c7a9-103">Skapar ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-103">Creates a network interface.</span></span>

## <span data-ttu-id="3c7a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c7a9-104">SYNTAX</span></span>

### <span data-ttu-id="3c7a9-105">SetByIpConfigurationResource (standard)</span><span class="sxs-lookup"><span data-stu-id="3c7a9-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c7a9-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="3c7a9-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-NetworkSecurityGroupId <String>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c7a9-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3c7a9-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c7a9-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3c7a9-108">SetByResource</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
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

## <span data-ttu-id="3c7a9-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c7a9-109">DESCRIPTION</span></span>
<span data-ttu-id="3c7a9-110">Cmdleten **New-AzNetworkInterface** skapar ett Azure-nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="3c7a9-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c7a9-111">EXAMPLES</span></span>

### <span data-ttu-id="3c7a9-112">Exempel 1: skapa ett Azure nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="3c7a9-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="3c7a9-113">Det här kommandot skapar ett nätverks gränssnitt med namnet NetworkInterface001 med en dynamiskt tilldelad privat IP-adress från Subnet1 i det virtuella nätverket med namnet VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="3c7a9-114">Kommandot tilldelar också två DNS-servrar till nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="3c7a9-115">Den underordnade resursen IPConfiguration skapas automatiskt med namnet IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="3c7a9-116">Exempel 2: skapa ett Azure nätverks gränssnitt med ett IP-konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="3c7a9-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="3c7a9-117">I det här exemplet skapas ett nytt nätverks gränssnitt med ett IP-konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="3c7a9-118">IP-konfigurationsobjektet anger en statisk privat IPv4-adress.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-118">The IP configuration object specifies a static private IPv4 address.</span></span>

<span data-ttu-id="3c7a9-119">Det första kommandot skapar en IP-konfiguration för ett nätverks gränssnitt med namnet IPConfig1 och lagrar konfigurationen i variabeln som heter $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>

<span data-ttu-id="3c7a9-120">Det andra kommandot skapar ett nätverks gränssnitt med namnet NetworkInterface1 som använder IP-konfigurationen för nätverks gränssnittet som lagras i variabeln $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="3c7a9-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c7a9-121">PARAMETERS</span></span>

### <span data-ttu-id="3c7a9-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3c7a9-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="3c7a9-123">Anger ett **ApplicationGatewayBackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="3c7a9-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="3c7a9-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="3c7a9-125">Anger ID för ett **ApplicationGatewayBackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="3c7a9-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3c7a9-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="3c7a9-127">Anger en samling med program säkerhets grupp referenser som nätverks gränssnittets IP-konfiguration ska tillhöra.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="3c7a9-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="3c7a9-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="3c7a9-129">Anger en samling med program säkerhets grupp referenser som nätverks gränssnittets IP-konfiguration ska tillhöra.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="3c7a9-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c7a9-130">-AsJob</span></span>
<span data-ttu-id="3c7a9-131">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3c7a9-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c7a9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c7a9-132">-DefaultProfile</span></span>
<span data-ttu-id="3c7a9-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c7a9-134">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="3c7a9-134">-DnsServer</span></span>
<span data-ttu-id="3c7a9-135">Anger DNS-server för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-135">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="3c7a9-136">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="3c7a9-136">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="3c7a9-137">Aktiverar snabbare nätverk.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-137">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="3c7a9-138">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="3c7a9-138">-EnableIPForwarding</span></span>
<span data-ttu-id="3c7a9-139">Anger att denna cmdlet aktiverar IP-vidarekoppling för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-139">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="3c7a9-140">Med IP-vidarebefordring kan en virtuell dator ta emot trafik adresserade till andra destinationer.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-140">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="3c7a9-141">-Force</span><span class="sxs-lookup"><span data-stu-id="3c7a9-141">-Force</span></span>
<span data-ttu-id="3c7a9-142">Tvingar skapandet av nätverks gränssnittet även om det finns ett nätverks gränssnitt med samma namn.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-142">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="3c7a9-143">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="3c7a9-143">-InternalDnsNameLabel</span></span>
<span data-ttu-id="3c7a9-144">Anger den interna DNS-etiketten för det nya nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-144">Specifies the internal DNS name label for the new network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7a9-145">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c7a9-145">-IpConfiguration</span></span>
<span data-ttu-id="3c7a9-146">Anger den IP-konfiguration som denna cmdlet använder för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-146">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="3c7a9-147">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3c7a9-147">-IpConfigurationName</span></span>
<span data-ttu-id="3c7a9-148">Anger namnet på en IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-148">Specifies the name of an IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7a9-149">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3c7a9-149">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="3c7a9-150">Anger ett **BackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-150">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="3c7a9-151">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="3c7a9-151">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="3c7a9-152">Anger ID för ett **BackendAddressPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-152">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="3c7a9-153">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="3c7a9-153">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="3c7a9-154">Anger en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-154">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="3c7a9-155">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="3c7a9-155">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="3c7a9-156">Anger ID för en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-156">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="3c7a9-157">-Plats</span><span class="sxs-lookup"><span data-stu-id="3c7a9-157">-Location</span></span>
<span data-ttu-id="3c7a9-158">Anger region för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-158">Specifies the region for a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7a9-159">-Namn</span><span class="sxs-lookup"><span data-stu-id="3c7a9-159">-Name</span></span>
<span data-ttu-id="3c7a9-160">Anger namnet på det nätverks gränssnitt som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-160">Specifies the name of the network interface to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7a9-161">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3c7a9-161">-NetworkSecurityGroup</span></span>
<span data-ttu-id="3c7a9-162">Anger ett **NetworkSecurityGroup** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-162">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: SetByIpConfigurationResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7a9-163">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="3c7a9-163">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="3c7a9-164">Anger ID för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-164">Specifies the ID of a network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByIpConfigurationResourceId, SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7a9-165">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="3c7a9-165">-PrivateIpAddress</span></span>
<span data-ttu-id="3c7a9-166">Anger en statisk IPv4-IP-adress att tilldela det här nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-166">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7a9-167">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3c7a9-167">-PublicIpAddress</span></span>
<span data-ttu-id="3c7a9-168">Anger ett **PublicIPAddress** -objekt som ska kopplas till ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-168">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7a9-169">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="3c7a9-169">-PublicIpAddressId</span></span>
<span data-ttu-id="3c7a9-170">Anger ID för ett **PublicIPAddress** -objekt som ska kopplas till ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-170">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7a9-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c7a9-171">-ResourceGroupName</span></span>
<span data-ttu-id="3c7a9-172">Anger namnet på en resurs grupp som nätverks gränssnittet tillhör.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-172">Specifies the name of a resource group that the network interface belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7a9-173">-Undernät</span><span class="sxs-lookup"><span data-stu-id="3c7a9-173">-Subnet</span></span>
<span data-ttu-id="3c7a9-174">Anger ett **under näts** objekt.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-174">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="3c7a9-175">Denna cmdlet skapar ett nätverks gränssnitt för det undernät som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-175">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7a9-176">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3c7a9-176">-SubnetId</span></span>
<span data-ttu-id="3c7a9-177">Anger ID för det undernät som du vill skapa ett nätverks gränssnitt för.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-177">Specifies the ID of the subnet for which to create a network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7a9-178">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3c7a9-178">-Tag</span></span>
<span data-ttu-id="3c7a9-179">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3c7a9-180">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="3c7a9-180">For example:</span></span>

<span data-ttu-id="3c7a9-181">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="3c7a9-181">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7a9-182">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3c7a9-182">-Confirm</span></span>
<span data-ttu-id="3c7a9-183">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-183">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c7a9-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c7a9-184">-WhatIf</span></span>
<span data-ttu-id="3c7a9-185">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c7a9-186">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-186">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c7a9-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c7a9-187">CommonParameters</span></span>
<span data-ttu-id="3c7a9-188">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c7a9-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c7a9-189">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c7a9-189">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c7a9-190">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c7a9-190">INPUTS</span></span>

## <span data-ttu-id="3c7a9-191">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c7a9-191">OUTPUTS</span></span>

### <span data-ttu-id="3c7a9-192">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3c7a9-192">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="3c7a9-193">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c7a9-193">NOTES</span></span>

## <span data-ttu-id="3c7a9-194">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c7a9-194">RELATED LINKS</span></span>

[<span data-ttu-id="3c7a9-195">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3c7a9-195">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="3c7a9-196">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3c7a9-196">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="3c7a9-197">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3c7a9-197">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
