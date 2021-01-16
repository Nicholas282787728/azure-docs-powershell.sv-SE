---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterface.md
ms.openlocfilehash: 1f49c2de253b41db97719933111a5ec2f9b861d5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393456"
---
# <span data-ttu-id="6ea13-101">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6ea13-101">Get-AzNetworkInterface</span></span>

## <span data-ttu-id="6ea13-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6ea13-102">SYNOPSIS</span></span>
<span data-ttu-id="6ea13-103">Hämtar ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="6ea13-103">Gets a network interface.</span></span>

## <span data-ttu-id="6ea13-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6ea13-104">SYNTAX</span></span>

### <span data-ttu-id="6ea13-105">NoExpandStandAloneNic (standard)</span><span class="sxs-lookup"><span data-stu-id="6ea13-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ea13-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="6ea13-106">ExpandStandAloneNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ea13-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="6ea13-107">NoExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ea13-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="6ea13-108">ExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ea13-109">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ea13-109">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkInterface -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ea13-110">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ea13-110">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkInterface -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ea13-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6ea13-111">DESCRIPTION</span></span>
<span data-ttu-id="6ea13-112">Cmdleten **Get-AzNetworkInterface** får ett Azure-nätverkskort eller en lista med Azure Network-gränssnitt i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6ea13-112">The **Get-AzNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="6ea13-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6ea13-113">EXAMPLES</span></span>

### <span data-ttu-id="6ea13-114">Exempel 1: skaffa alla nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="6ea13-114">Example 1: Get all network interfaces</span></span>
```
PS C:\> Get-AzNetworkInterface

Name                        : test1
ResourceGroupName           : ResourceGroup1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/providers/Micros
                              oft.Network/networkInterfaces/test1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Compute/virtualMachines/test1"
                              }
IpConfigurations            : [
                                {
                                  "Name": "test1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provi
                              ders/Microsoft.Network/networkInterfaces/test1/ipConfigurations/test1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/virtualNetworks/test1/subnets/test1",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/publicIPAddresses/test1"
                                  },
                                  "ProvisioningState": "Succeeded",
                                  "PrivateIpAddressVersion": "IPv4",
                                  "LoadBalancerBackendAddressPools": [],
                                  "LoadBalancerInboundNatRules": [],
                                  "Primary": true,
                                  "ApplicationGatewayBackendAddressPools": [],
                                  "ApplicationSecurityGroups": []
                                }
                              ]
DnsSettings                 : {
                                "DnsServers": [],
                                "AppliedDnsServers": []
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Network/networkSecurityGroups/test1"
                              }
Primary                     : True
MacAddress                  :
```

<span data-ttu-id="6ea13-115">Det här kommandot får alla nätverks gränssnitt för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6ea13-115">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="6ea13-116">Exempel 2: Hämta alla nätverks gränssnitt med ett specifikt etablerings tillstånd</span><span class="sxs-lookup"><span data-stu-id="6ea13-116">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}

Name                        : test1
ResourceGroupName           : ResourceGroup1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/providers/Micros
                              oft.Network/networkInterfaces/test1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Compute/virtualMachines/test1"
                              }
IpConfigurations            : [
                                {
                                  "Name": "test1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provi
                              ders/Microsoft.Network/networkInterfaces/test1/ipConfigurations/test1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/virtualNetworks/test1/subnets/test1",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/publicIPAddresses/test1"
                                  },
                                  "ProvisioningState": "Succeeded",
                                  "PrivateIpAddressVersion": "IPv4",
                                  "LoadBalancerBackendAddressPools": [],
                                  "LoadBalancerInboundNatRules": [],
                                  "Primary": true,
                                  "ApplicationGatewayBackendAddressPools": [],
                                  "ApplicationSecurityGroups": []
                                }
                              ]
DnsSettings                 : {
                                "DnsServers": [],
                                "AppliedDnsServers": []
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Network/networkSecurityGroups/test1"
                              }
Primary                     : True
MacAddress                  :
```

<span data-ttu-id="6ea13-117">Det här kommandot får alla nätverks gränssnitt i resurs gruppen som heter ResourceGroup1 och som har ett etablerings tillstånd.</span><span class="sxs-lookup"><span data-stu-id="6ea13-117">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

### <span data-ttu-id="6ea13-118">Exempel 3: skaffa nätverks gränssnitt med filter</span><span class="sxs-lookup"><span data-stu-id="6ea13-118">Example 3: Get network interfaces using filtering</span></span>
```
PS C:\> Get-AzNetworkInterface -Name test*

Name                        : test1
ResourceGroupName           : ResourceGroup1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/providers/Micros
                              oft.Network/networkInterfaces/test1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Compute/virtualMachines/test1"
                              }
IpConfigurations            : [
                                {
                                  "Name": "test1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provi
                              ders/Microsoft.Network/networkInterfaces/test1/ipConfigurations/test1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/virtualNetworks/test1/subnets/test1",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/publicIPAddresses/test1"
                                  },
                                  "ProvisioningState": "Succeeded",
                                  "PrivateIpAddressVersion": "IPv4",
                                  "LoadBalancerBackendAddressPools": [],
                                  "LoadBalancerInboundNatRules": [],
                                  "Primary": true,
                                  "ApplicationGatewayBackendAddressPools": [],
                                  "ApplicationSecurityGroups": []
                                }
                              ]
DnsSettings                 : {
                                "DnsServers": [],
                                "AppliedDnsServers": []
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Network/networkSecurityGroups/test1"
                              }
Primary                     : True
MacAddress                  :
```

<span data-ttu-id="6ea13-119">Det här kommandot får alla nätverks gränssnitt för det aktuella abonnemanget som börjar med "test".</span><span class="sxs-lookup"><span data-stu-id="6ea13-119">This command gets all network interfaces for the current subscription that start with "test".</span></span>

## <span data-ttu-id="6ea13-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6ea13-120">PARAMETERS</span></span>

### <span data-ttu-id="6ea13-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ea13-121">-DefaultProfile</span></span>
<span data-ttu-id="6ea13-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6ea13-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ea13-123">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="6ea13-123">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic, GetByResourceIdExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ea13-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="6ea13-124">-Name</span></span>
<span data-ttu-id="6ea13-125">Anger namnet på det nätverks gränssnitt som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="6ea13-125">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6ea13-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ea13-126">-ResourceGroupName</span></span>
<span data-ttu-id="6ea13-127">Anger namnet på den resurs grupp från vilken denna cmdlet får nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="6ea13-127">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6ea13-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ea13-128">-ResourceId</span></span>
<span data-ttu-id="6ea13-129">Azure Resource Manager-ID för nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="6ea13-129">The Azure resource manager id of the network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ea13-130">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="6ea13-130">-VirtualMachineIndex</span></span>
<span data-ttu-id="6ea13-131">Anger det virtuella dator indexet för den virtuella datorns skal uppsättning som denna cmdlet hämtar nätverks gränssnitten från.</span><span class="sxs-lookup"><span data-stu-id="6ea13-131">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ea13-132">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6ea13-132">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="6ea13-133">Anger namnet på den skalnings uppsättning för virtuell dator från vilken denna cmdlet hämtar nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="6ea13-133">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ea13-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ea13-134">CommonParameters</span></span>
<span data-ttu-id="6ea13-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ea13-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ea13-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ea13-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ea13-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6ea13-137">INPUTS</span></span>

### <span data-ttu-id="6ea13-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6ea13-138">System.String</span></span>

## <span data-ttu-id="6ea13-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6ea13-139">OUTPUTS</span></span>

### <span data-ttu-id="6ea13-140">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6ea13-140">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="6ea13-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6ea13-141">NOTES</span></span>

## <span data-ttu-id="6ea13-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6ea13-142">RELATED LINKS</span></span>

[<span data-ttu-id="6ea13-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6ea13-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="6ea13-144">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6ea13-144">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="6ea13-145">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6ea13-145">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


