---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzBastion.md
ms.openlocfilehash: e2e2feacaefb0ce29c77263c0b733f503b8e9a74
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271786"
---
# <span data-ttu-id="7bd68-101">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="7bd68-101">New-AzBastion</span></span>

## <span data-ttu-id="7bd68-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7bd68-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd68-103">Skapar en Bastion-resurs.</span><span class="sxs-lookup"><span data-stu-id="7bd68-103">Creates a bastion resource.</span></span>

## <span data-ttu-id="7bd68-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7bd68-104">SYNTAX</span></span>

### <span data-ttu-id="7bd68-105">ByPublicIpAddressByVirtualNetwork (standard)</span><span class="sxs-lookup"><span data-stu-id="7bd68-105">ByPublicIpAddressByVirtualNetwork (Default)</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bd68-106">ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="7bd68-106">ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bd68-107">ByPublicIpAddressByVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="7bd68-107">ByPublicIpAddressByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetworkId <String> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bd68-108">ByPublicIpAddressIdByVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7bd68-108">ByPublicIpAddressIdByVirtualNetwork</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String>
 -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bd68-109">ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="7bd68-109">ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String>
 -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bd68-110">ByPublicIpAddressIdByVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="7bd68-110">ByPublicIpAddressIdByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String> -VirtualNetworkId <String>
 [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7bd68-111">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7bd68-111">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bd68-112">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="7bd68-112">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bd68-113">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="7bd68-113">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetworkId <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bd68-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7bd68-114">DESCRIPTION</span></span>
<span data-ttu-id="7bd68-115">Skapar en Bastion-resurs. Detta kommer att behöva en offentlig IP-adress och VirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="7bd68-115">Creates a bastion resource.This will need a Public Ip Address and a VirtualNetwork.</span></span> <span data-ttu-id="7bd68-116">Det måste finnas ett undernät med namnet AzureBastionSubnet i den här VirtualNetwork. kuk-IP-adressen måste skapas med SKU-standarden.</span><span class="sxs-lookup"><span data-stu-id="7bd68-116">There must be a subnet with name AzureBastionSubnet in this VirtualNetwork.The Pubic Ip Address must be created with Sku Standard.</span></span>

## <span data-ttu-id="7bd68-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7bd68-117">EXAMPLES</span></span>

### <span data-ttu-id="7bd68-118">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7bd68-118">Example 1</span></span>
```powershell
$subnetName = "AzureBastionSubnet"
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name "TestVnet" -ResourceGroupName "BastionPowershellTest" -Location "westeurope" -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$publicip = New-AzPublicIpAddress -ResourceGroupName "BastionPowershellTest" -name "Test-Ip" -location "westeurope" -AllocationMethod Dynamic -Sku Standard
$bastion = New-AzBastion -ResourceGroupName "BastionPowershellTest" â€“Name "test-Bastion2" -PublicIpAddress $publicip -VirtualNetwork $vnet

IpConfigurations     : {IpConf}
DnsName              : bst-a9ca868f-ddab-4a50-9f45-a443ea8a0187.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/virtualNetworks/TestVnet/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/publicIPAddresses/Test-Ip"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic",
                           "Name": "IpConf",
                           "Etag": "W/\"ed810ccd-b3f6-4e22-891e-b0ed0a26d6dd\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/test-Bastion2/bastionHostIpConfigurations/IpConf"
                         }
                       ]
ResourceGroupName    : BastionPowershellTest
Location             : westeurope
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  :
TagsTable            :
Name                 : test-Bastion2
Etag                 : W/"ed810ccd-b3f6-4e22-891e-b0ed0a26d6dd"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/test-Bastion2

This example creates a bastion attached to virtual network "vnet" in the same resource group as the bastion.
There must be a subnet with name AzureBastionSubnet in this vnet.
The Ip Address must be created with Sku Standard.
```

### <span data-ttu-id="7bd68-119">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7bd68-119">Example 2</span></span>
```powershell
$vnet = Get-AzVirtualNetwork -ResourceGroupName "BastionPowershellTest" -Name "testVnet2"
Add-AzVirtualNetworkSubnetConfig -Name "AzureBastionSubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.0.0/24"
$vnet| Set-AzVirtualNetwork
New-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2" -PublicIpAddressRgName "BastionPowershellTest" -PublicIpAddressName "testIp2" -VirtualNetworkRgName "BastionPowershellTest" -VirtualNetworkName "testVnet2"

IpConfigurations     : {IpConf}
DnsName              : bst-53757658-c4fd-4908-b1a7-0849e555d489.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Name": "IpConf",
                           "Etag": "W/\"7460e5f6-ad41-438b-a595-a63346ed8f16\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/testBastion2/bastionHostIpConfigurations/IpConf",
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/virtualNetworks/testVnet2/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/publicIPAddresses/testIp2"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic"
                         }
                       ]
ResourceGroupName    : BastionPowershellTest
Location             : westeurope
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  :
TagsTable            :
Name                 : testBastion2
Etag                 : W/"7460e5f6-ad41-438b-a595-a63346ed8f16"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/testBastion2
```

## <span data-ttu-id="7bd68-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7bd68-120">PARAMETERS</span></span>

### <span data-ttu-id="7bd68-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bd68-121">-AsJob</span></span>
<span data-ttu-id="7bd68-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7bd68-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7bd68-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7bd68-123">-Confirm</span></span>
<span data-ttu-id="7bd68-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7bd68-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd68-125">-DefaultProfile</span></span>
<span data-ttu-id="7bd68-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7bd68-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="7bd68-127">-Name</span></span>
<span data-ttu-id="7bd68-128">Bastion resurs namn.</span><span class="sxs-lookup"><span data-stu-id="7bd68-128">The bastion resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-129">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7bd68-129">-PublicIpAddress</span></span>
<span data-ttu-id="7bd68-130">Den offentliga IP-adressen för Bastion.</span><span class="sxs-lookup"><span data-stu-id="7bd68-130">The public IP address object for bastion.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: ByPublicIpAddressByVirtualNetwork, ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressByVirtualNetworkId
Aliases: PublicIpAddressObject

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-131">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="7bd68-131">-PublicIpAddressId</span></span>
<span data-ttu-id="7bd68-132">Den offentliga IP-adressens Azure-ID för Bastion.</span><span class="sxs-lookup"><span data-stu-id="7bd68-132">The public Ip address Azure resource Id for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressIdByVirtualNetwork, ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressIdByVirtualNetworkId
Aliases: PublicIpAddressResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-133">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="7bd68-133">-PublicIpAddressName</span></span>
<span data-ttu-id="7bd68-134">Den offentliga IP-adressens resurs namn för Bastion.</span><span class="sxs-lookup"><span data-stu-id="7bd68-134">The public Ip address resource name for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-135">-PublicIpAddressRgName</span><span class="sxs-lookup"><span data-stu-id="7bd68-135">-PublicIpAddressRgName</span></span>
<span data-ttu-id="7bd68-136">Resurs grupp namnet för offentlig IP-adress för Bastion.</span><span class="sxs-lookup"><span data-stu-id="7bd68-136">The public Ip address resource group name for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId
Aliases: PublicIpAddressResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bd68-137">-ResourceGroupName</span></span>
<span data-ttu-id="7bd68-138">Namnet på resurs gruppen där du måste skapa Bastion.</span><span class="sxs-lookup"><span data-stu-id="7bd68-138">The resource group name where you need to create bastion.</span></span>

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

### <span data-ttu-id="7bd68-139">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7bd68-139">-Tag</span></span>
<span data-ttu-id="7bd68-140">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="7bd68-140">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-141">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7bd68-141">-VirtualNetwork</span></span>
<span data-ttu-id="7bd68-142">Det virtuella nätverks objekt för Bastion.</span><span class="sxs-lookup"><span data-stu-id="7bd68-142">The virtual network object for bastion.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByPublicIpAddressByVirtualNetwork, ByPublicIpAddressIdByVirtualNetwork, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork
Aliases: VirtualNetworkObject

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-143">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="7bd68-143">-VirtualNetworkId</span></span>
<span data-ttu-id="7bd68-144">Det virtuella nätverkets ID för Azure-resurs för Bastion.</span><span class="sxs-lookup"><span data-stu-id="7bd68-144">The virtual network Azure resource Id for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressByVirtualNetworkId, ByPublicIpAddressIdByVirtualNetworkId, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId
Aliases: VirtualNetworkResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-145">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="7bd68-145">-VirtualNetworkName</span></span>
<span data-ttu-id="7bd68-146">Namnet på den virtuella nätverks resursen för Bastion.</span><span class="sxs-lookup"><span data-stu-id="7bd68-146">The virtual network resource name for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-147">-VirtualNetworkRgName</span><span class="sxs-lookup"><span data-stu-id="7bd68-147">-VirtualNetworkRgName</span></span>
<span data-ttu-id="7bd68-148">Den virtuella nätverks resurs gruppens namn för Bastion.</span><span class="sxs-lookup"><span data-stu-id="7bd68-148">The virtual network resource group name for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName
Aliases: VirtualNetworkResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bd68-149">-WhatIf</span></span>
<span data-ttu-id="7bd68-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7bd68-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bd68-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7bd68-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd68-152">CommonParameters</span></span>
<span data-ttu-id="7bd68-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bd68-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd68-154">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bd68-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd68-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7bd68-155">INPUTS</span></span>

### <span data-ttu-id="7bd68-156">Ingen</span><span class="sxs-lookup"><span data-stu-id="7bd68-156">None</span></span>

## <span data-ttu-id="7bd68-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7bd68-157">OUTPUTS</span></span>

### <span data-ttu-id="7bd68-158">Microsoft. Azure. commands. Networks. Models. PSBastion</span><span class="sxs-lookup"><span data-stu-id="7bd68-158">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

## <span data-ttu-id="7bd68-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7bd68-159">NOTES</span></span>

## <span data-ttu-id="7bd68-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7bd68-160">RELATED LINKS</span></span>
[<span data-ttu-id="7bd68-161">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="7bd68-161">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="7bd68-162">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="7bd68-162">Remove-AzBastion</span></span>](./Remove-AzBastion.md)