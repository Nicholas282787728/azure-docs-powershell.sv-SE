---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: b7ed573ed8df8086cd5cef04204020498e1413c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395339"
---
# <span data-ttu-id="eb285-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="eb285-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="eb285-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb285-102">SYNOPSIS</span></span>
<span data-ttu-id="eb285-103">Uppdaterar en VPN-webbplats.</span><span class="sxs-lookup"><span data-stu-id="eb285-103">Updates a VPN site.</span></span>

## <span data-ttu-id="eb285-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb285-104">SYNTAX</span></span>

### <span data-ttu-id="eb285-105">ByVpnSiteNameNoVirtualWanUpdate (standard)</span><span class="sxs-lookup"><span data-stu-id="eb285-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb285-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="eb285-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb285-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="eb285-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb285-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="eb285-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb285-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="eb285-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb285-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="eb285-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb285-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="eb285-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb285-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="eb285-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb285-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="eb285-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb285-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="eb285-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb285-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="eb285-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb285-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="eb285-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb285-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb285-117">DESCRIPTION</span></span>
<span data-ttu-id="eb285-118">Cmdleten **Update-AzVpnSite** uppdaterar en VPN-webbplats.</span><span class="sxs-lookup"><span data-stu-id="eb285-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="eb285-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb285-119">EXAMPLES</span></span>

### <span data-ttu-id="eb285-120">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eb285-120">Example 1</span></span>

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

<span data-ttu-id="eb285-121">Ovanstående skapar en resurs grupp, virtuellt WAN i West-resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="eb285-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="eb285-122">Därefter skapas en VpnSite för att representera en kund gren och länkar den till den virtuella WAN-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="eb285-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="eb285-123">När webbplatsen har skapats uppdaterar den IpAddress för webbplatsen med kommandot Set-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="eb285-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="eb285-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb285-124">PARAMETERS</span></span>

### <span data-ttu-id="eb285-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="eb285-125">-AddressSpace</span></span>
<span data-ttu-id="eb285-126">Adressprefix för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="eb285-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="eb285-127">Använd den här eller AddressSpaceObject, men inte båda.</span><span class="sxs-lookup"><span data-stu-id="eb285-127">Use this or AddressSpaceObject but not both.</span></span>

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

### <span data-ttu-id="eb285-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb285-128">-AsJob</span></span>
<span data-ttu-id="eb285-129">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="eb285-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb285-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="eb285-130">-BgpAsn</span></span>
<span data-ttu-id="eb285-131">BGP ASN för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="eb285-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="eb285-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="eb285-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="eb285-133">BGP peering-adressen för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="eb285-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="eb285-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="eb285-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="eb285-135">BGP-peering-vikten för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="eb285-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="eb285-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb285-136">-DefaultProfile</span></span>
<span data-ttu-id="eb285-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eb285-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb285-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="eb285-138">-DeviceModel</span></span>
<span data-ttu-id="eb285-139">Enhets modellen för fjärr-VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="eb285-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="eb285-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="eb285-140">-DeviceVendor</span></span>
<span data-ttu-id="eb285-141">Enhets leverantören för fjärr-VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="eb285-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="eb285-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb285-142">-InputObject</span></span>
<span data-ttu-id="eb285-143">VPN-objektet som ska ändras</span><span class="sxs-lookup"><span data-stu-id="eb285-143">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="eb285-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="eb285-144">-IpAddress</span></span>
<span data-ttu-id="eb285-145">IP-adress för lokal nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="eb285-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="eb285-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="eb285-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="eb285-147">Enhets modellen för fjärr-VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="eb285-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="eb285-148">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb285-148">-Name</span></span>
<span data-ttu-id="eb285-149">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="eb285-149">The resource name.</span></span>

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

### <span data-ttu-id="eb285-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="eb285-150">-O365Policy</span></span>
<span data-ttu-id="eb285-151">Översikten policy för Office 365 för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="eb285-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb285-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb285-152">-ResourceGroupName</span></span>
<span data-ttu-id="eb285-153">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="eb285-153">The resource group name.</span></span>

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

### <span data-ttu-id="eb285-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb285-154">-ResourceId</span></span>
<span data-ttu-id="eb285-155">Azure Resource ID för VPN-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="eb285-155">The Azure resource ID for the vpn site.</span></span>

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

### <span data-ttu-id="eb285-156">-Tagg</span><span class="sxs-lookup"><span data-stu-id="eb285-156">-Tag</span></span>
<span data-ttu-id="eb285-157">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="eb285-157">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="eb285-158">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="eb285-158">-VirtualWan</span></span>
<span data-ttu-id="eb285-159">VirtualWan denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="eb285-159">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="eb285-160">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="eb285-160">-VirtualWanId</span></span>
<span data-ttu-id="eb285-161">ResourceId-VirtualWan som denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="eb285-161">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="eb285-162">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="eb285-162">-VirtualWanName</span></span>
<span data-ttu-id="eb285-163">Namnet på den VirtualWan som denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="eb285-163">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="eb285-164">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb285-164">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="eb285-165">Namnet på den VirtualWan som denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="eb285-165">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="eb285-166">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="eb285-166">-VpnSiteLink</span></span>
<span data-ttu-id="eb285-167">Listan med VpnSiteLinks som denna VpnSite har.</span><span class="sxs-lookup"><span data-stu-id="eb285-167">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="eb285-168">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eb285-168">-Confirm</span></span>
<span data-ttu-id="eb285-169">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eb285-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb285-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb285-170">-WhatIf</span></span>
<span data-ttu-id="eb285-171">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eb285-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb285-172">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eb285-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb285-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb285-173">CommonParameters</span></span>
<span data-ttu-id="eb285-174">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb285-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb285-175">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb285-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb285-176">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb285-176">INPUTS</span></span>

### <span data-ttu-id="eb285-177">Microsoft. Azure. commands. Networks. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="eb285-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="eb285-178">System. String</span><span class="sxs-lookup"><span data-stu-id="eb285-178">System.String</span></span>

## <span data-ttu-id="eb285-179">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb285-179">OUTPUTS</span></span>

### <span data-ttu-id="eb285-180">Microsoft. Azure. commands. Networks. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="eb285-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="eb285-181">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb285-181">NOTES</span></span>

## <span data-ttu-id="eb285-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb285-182">RELATED LINKS</span></span>

[<span data-ttu-id="eb285-183">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="eb285-183">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="eb285-184">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="eb285-184">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="eb285-185">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="eb285-185">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)
