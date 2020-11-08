---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: 271d86db8cd67f75d27e94a5a5dea851cfc9e3b7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092234"
---
# <span data-ttu-id="975e8-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="975e8-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="975e8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="975e8-102">SYNOPSIS</span></span>
<span data-ttu-id="975e8-103">Uppdaterar en VPN-webbplats.</span><span class="sxs-lookup"><span data-stu-id="975e8-103">Updates a VPN site.</span></span>

## <span data-ttu-id="975e8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="975e8-104">SYNTAX</span></span>

### <span data-ttu-id="975e8-105">ByVpnSiteNameNoVirtualWanUpdate (standard)</span><span class="sxs-lookup"><span data-stu-id="975e8-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="975e8-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="975e8-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="975e8-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="975e8-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="975e8-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="975e8-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="975e8-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="975e8-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="975e8-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="975e8-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="975e8-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="975e8-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="975e8-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="975e8-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="975e8-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="975e8-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="975e8-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="975e8-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="975e8-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="975e8-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="975e8-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="975e8-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="975e8-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="975e8-117">DESCRIPTION</span></span>
<span data-ttu-id="975e8-118">Cmdleten **Update-AzVpnSite** uppdaterar en VPN-webbplats.</span><span class="sxs-lookup"><span data-stu-id="975e8-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="975e8-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="975e8-119">EXAMPLES</span></span>

### <span data-ttu-id="975e8-120">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="975e8-120">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "2.3.5.5"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 2.3.4.5
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="975e8-121">Ovanstående skapar en resurs grupp, virtuellt WAN i West-resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="975e8-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="975e8-122">Därefter skapas en VpnSite för att representera en kund gren och länkar den till den virtuella WAN-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="975e8-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="975e8-123">När webbplatsen har skapats uppdaterar den IpAddress för webbplatsen med kommandot Set-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="975e8-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="975e8-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="975e8-124">PARAMETERS</span></span>

### <span data-ttu-id="975e8-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="975e8-125">-AddressSpace</span></span>
<span data-ttu-id="975e8-126">Adressprefix för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="975e8-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="975e8-127">Använd den här eller AddressSpaceObject, men inte båda.</span><span class="sxs-lookup"><span data-stu-id="975e8-127">Use this or AddressSpaceObject but not both.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975e8-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="975e8-128">-AsJob</span></span>
<span data-ttu-id="975e8-129">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="975e8-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="975e8-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="975e8-130">-BgpAsn</span></span>
<span data-ttu-id="975e8-131">BGP ASN för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="975e8-131">The BGP ASN for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975e8-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="975e8-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="975e8-133">BGP peering-adressen för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="975e8-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="975e8-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="975e8-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="975e8-135">BGP-peering-vikten för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="975e8-135">The BGP Peering weight for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975e8-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="975e8-136">-DefaultProfile</span></span>
<span data-ttu-id="975e8-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="975e8-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="975e8-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="975e8-138">-DeviceModel</span></span>
<span data-ttu-id="975e8-139">Enhets modellen för fjärr-VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="975e8-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="975e8-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="975e8-140">-DeviceVendor</span></span>
<span data-ttu-id="975e8-141">Enhets leverantören för fjärr-VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="975e8-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="975e8-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="975e8-142">-InputObject</span></span>
<span data-ttu-id="975e8-143">VPN-objektet som ska ändras</span><span class="sxs-lookup"><span data-stu-id="975e8-143">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObjectByVirtualWanName, ByVpnSiteObjectByVirtualWanResourceId, ByVpnSiteObjectByVirtualWanObject, ByVpnSiteObjectNoVirtualWanUpdate
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="975e8-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="975e8-144">-IpAddress</span></span>
<span data-ttu-id="975e8-145">IP-adress för lokal nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="975e8-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="975e8-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="975e8-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="975e8-147">Enhets modellen för fjärr-VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="975e8-147">The device model of the remote vpn device.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975e8-148">-Namn</span><span class="sxs-lookup"><span data-stu-id="975e8-148">-Name</span></span>
<span data-ttu-id="975e8-149">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="975e8-149">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameNoVirtualWanUpdate, ByVpnSiteNameByVirtualWanName, ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteNameByVirtualWanObject
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975e8-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="975e8-150">-ResourceGroupName</span></span>
<span data-ttu-id="975e8-151">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="975e8-151">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameNoVirtualWanUpdate, ByVpnSiteNameByVirtualWanName, ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteNameByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975e8-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="975e8-152">-ResourceId</span></span>
<span data-ttu-id="975e8-153">Azure Resource ID för VPN-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="975e8-153">The Azure resource ID for the vpn site.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceIdByVirtualWanName, ByVpnSiteResourceIdByVirtualWanResourceId, ByVpnSiteResourceIdByVirtualWanObject, ByVpnSiteResourceIdNoVirtualWanUpdate
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="975e8-154">-Tagg</span><span class="sxs-lookup"><span data-stu-id="975e8-154">-Tag</span></span>
<span data-ttu-id="975e8-155">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="975e8-155">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975e8-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="975e8-156">-VirtualWan</span></span>
<span data-ttu-id="975e8-157">VirtualWan denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="975e8-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVpnSiteNameByVirtualWanObject, ByVpnSiteObjectByVirtualWanObject, ByVpnSiteResourceIdByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975e8-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="975e8-158">-VirtualWanId</span></span>
<span data-ttu-id="975e8-159">ResourceId-VirtualWan som denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="975e8-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteObjectByVirtualWanResourceId, ByVpnSiteResourceIdByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975e8-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="975e8-160">-VirtualWanName</span></span>
<span data-ttu-id="975e8-161">Namnet på den VirtualWan som denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="975e8-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanName, ByVpnSiteObjectByVirtualWanName, ByVpnSiteResourceIdByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975e8-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="975e8-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="975e8-163">Namnet på den VirtualWan som denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="975e8-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanName, ByVpnSiteObjectByVirtualWanName, ByVpnSiteResourceIdByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975e8-164">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="975e8-164">-VpnSiteLink</span></span>
<span data-ttu-id="975e8-165">Listan med VpnSiteLinks som denna VpnSite har.</span><span class="sxs-lookup"><span data-stu-id="975e8-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975e8-166">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="975e8-166">-Confirm</span></span>
<span data-ttu-id="975e8-167">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="975e8-167">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975e8-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="975e8-168">-WhatIf</span></span>
<span data-ttu-id="975e8-169">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="975e8-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="975e8-170">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="975e8-170">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975e8-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="975e8-171">CommonParameters</span></span>
<span data-ttu-id="975e8-172">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="975e8-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="975e8-173">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="975e8-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="975e8-174">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="975e8-174">INPUTS</span></span>

### <span data-ttu-id="975e8-175">Microsoft. Azure. commands. Networks. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="975e8-175">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="975e8-176">System. String</span><span class="sxs-lookup"><span data-stu-id="975e8-176">System.String</span></span>

## <span data-ttu-id="975e8-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="975e8-177">OUTPUTS</span></span>

### <span data-ttu-id="975e8-178">Microsoft. Azure. commands. Networks. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="975e8-178">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="975e8-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="975e8-179">NOTES</span></span>

## <span data-ttu-id="975e8-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="975e8-180">RELATED LINKS</span></span>

[<span data-ttu-id="975e8-181">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="975e8-181">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="975e8-182">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="975e8-182">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="975e8-183">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="975e8-183">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)