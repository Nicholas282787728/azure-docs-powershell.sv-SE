---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnSite.md
ms.openlocfilehash: fa24f61d0e638cb38e7cf882aac2191a5119b1b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578843"
---
# <span data-ttu-id="71149-101">Update-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="71149-101">Update-AzureRmVpnSite</span></span>

## <span data-ttu-id="71149-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71149-102">SYNOPSIS</span></span>
<span data-ttu-id="71149-103">Uppdaterar en VpnSite som representerar en kund filial till en avsedd mål status.</span><span class="sxs-lookup"><span data-stu-id="71149-103">Updates a VpnSite representing a customer branch to an intended goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71149-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71149-104">SYNTAX</span></span>

### <span data-ttu-id="71149-105">ByVpnSiteNameNoVirtualWanUpdate (standard)</span><span class="sxs-lookup"><span data-stu-id="71149-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzureRmVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71149-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="71149-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71149-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="71149-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71149-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="71149-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan>
 [-IpAddress <String>] [-AddressSpace <System.Collections.Generic.List`1[System.String]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71149-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="71149-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzureRmVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <System.Collections.Generic.List`1[System.String]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71149-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="71149-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzureRmVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71149-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="71149-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzureRmVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71149-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="71149-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzureRmVpnSite -InputObject <PSVpnSite> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71149-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="71149-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzureRmVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <System.Collections.Generic.List`1[System.String]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71149-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="71149-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzureRmVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71149-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="71149-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzureRmVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71149-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="71149-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzureRmVpnSite -ResourceId <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71149-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71149-117">DESCRIPTION</span></span>
<span data-ttu-id="71149-118">Uppdaterar en VpnSite som representerar en kund filial till en avsedd mål status.</span><span class="sxs-lookup"><span data-stu-id="71149-118">Updates a VpnSite representing a customer branch to an intended goal state.</span></span>

## <span data-ttu-id="71149-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71149-119">EXAMPLES</span></span>

### <span data-ttu-id="71149-120">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="71149-120">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "2.3.5.5"

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

<span data-ttu-id="71149-121">Ovanstående skapar en resurs grupp, virtuellt WAN i West-resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="71149-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="71149-122">Därefter skapas en VpnSite för att representera en kund gren och länkar den till den virtuella WAN-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="71149-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="71149-123">När webbplatsen har skapats uppdaterar den IpAddress för webbplatsen med kommandot Set-AzureRmVpnSite.</span><span class="sxs-lookup"><span data-stu-id="71149-123">Once the site is created, it updates the IpAddress of the site using the Set-AzureRmVpnSite command.</span></span>

## <span data-ttu-id="71149-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71149-124">PARAMETERS</span></span>

### <span data-ttu-id="71149-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="71149-125">-AddressSpace</span></span>
<span data-ttu-id="71149-126">Adressprefix för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="71149-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="71149-127">Använd den här eller AddressSpaceObject, men inte båda.</span><span class="sxs-lookup"><span data-stu-id="71149-127">Use this or AddressSpaceObject but not both.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71149-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71149-128">-AsJob</span></span>
<span data-ttu-id="71149-129">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="71149-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71149-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="71149-130">-BgpAsn</span></span>
<span data-ttu-id="71149-131">BGP ASN för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="71149-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="71149-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="71149-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="71149-133">BGP peering-adressen för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="71149-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="71149-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="71149-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="71149-135">BGP-peering-vikten för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="71149-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="71149-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71149-136">-DefaultProfile</span></span>
<span data-ttu-id="71149-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="71149-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71149-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="71149-138">-DeviceModel</span></span>
<span data-ttu-id="71149-139">Enhets modellen för fjärr-VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="71149-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="71149-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="71149-140">-DeviceVendor</span></span>
<span data-ttu-id="71149-141">Enhets leverantören för fjärr-VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="71149-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="71149-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71149-142">-InputObject</span></span>
<span data-ttu-id="71149-143">VPN-objektet som ska ändras</span><span class="sxs-lookup"><span data-stu-id="71149-143">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="71149-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="71149-144">-IpAddress</span></span>
<span data-ttu-id="71149-145">IP-adress för lokal nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="71149-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="71149-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="71149-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="71149-147">Enhets modellen för fjärr-VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="71149-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="71149-148">-Namn</span><span class="sxs-lookup"><span data-stu-id="71149-148">-Name</span></span>
<span data-ttu-id="71149-149">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="71149-149">The resource name.</span></span>

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

### <span data-ttu-id="71149-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71149-150">-ResourceGroupName</span></span>
<span data-ttu-id="71149-151">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="71149-151">The resource group name.</span></span>

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

### <span data-ttu-id="71149-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71149-152">-ResourceId</span></span>
<span data-ttu-id="71149-153">Azure Resource ID för VPN-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="71149-153">The Azure resource ID for the vpn site.</span></span>

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

### <span data-ttu-id="71149-154">-Tagg</span><span class="sxs-lookup"><span data-stu-id="71149-154">-Tag</span></span>
<span data-ttu-id="71149-155">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="71149-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="71149-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="71149-156">-VirtualWan</span></span>
<span data-ttu-id="71149-157">VirtualWan denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="71149-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="71149-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="71149-158">-VirtualWanId</span></span>
<span data-ttu-id="71149-159">ResourceId-VirtualWan som denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="71149-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="71149-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="71149-160">-VirtualWanName</span></span>
<span data-ttu-id="71149-161">Namnet på den VirtualWan som denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="71149-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="71149-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71149-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="71149-163">Namnet på den VirtualWan som denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="71149-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="71149-164">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="71149-164">-Confirm</span></span>
<span data-ttu-id="71149-165">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="71149-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71149-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71149-166">-WhatIf</span></span>
<span data-ttu-id="71149-167">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="71149-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71149-168">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="71149-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71149-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71149-169">CommonParameters</span></span>
<span data-ttu-id="71149-170">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71149-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71149-171">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71149-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71149-172">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71149-172">INPUTS</span></span>

### <span data-ttu-id="71149-173">Microsoft. Azure. commands. Networks. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="71149-173">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="71149-174">System. String</span><span class="sxs-lookup"><span data-stu-id="71149-174">System.String</span></span>

## <span data-ttu-id="71149-175">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71149-175">OUTPUTS</span></span>

### <span data-ttu-id="71149-176">Microsoft. Azure. commands. Networks. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="71149-176">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="71149-177">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71149-177">NOTES</span></span>

## <span data-ttu-id="71149-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71149-178">RELATED LINKS</span></span>
