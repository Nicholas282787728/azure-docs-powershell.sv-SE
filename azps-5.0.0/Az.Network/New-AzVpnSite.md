---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: ac203d499674e97080edd645f9643b12291873d1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325877"
---
# <span data-ttu-id="684e2-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="684e2-101">New-AzVpnSite</span></span>

## <span data-ttu-id="684e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="684e2-102">SYNOPSIS</span></span>
<span data-ttu-id="684e2-103">Skapar en ny Azure VpnSite-resurs.</span><span class="sxs-lookup"><span data-stu-id="684e2-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="684e2-104">Det här är en RM-representation av kund grenar som laddas upp till Azure för S2S-anslutning med en cortex virtuellt hubb.</span><span class="sxs-lookup"><span data-stu-id="684e2-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="684e2-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="684e2-105">SYNTAX</span></span>

### <span data-ttu-id="684e2-106">ByVirtualWanNameByVpnSiteIpAddress (standard)</span><span class="sxs-lookup"><span data-stu-id="684e2-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="684e2-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="684e2-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="684e2-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="684e2-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="684e2-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="684e2-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="684e2-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="684e2-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="684e2-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="684e2-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="684e2-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="684e2-112">DESCRIPTION</span></span>
<span data-ttu-id="684e2-113">Skapar en ny Azure VpnSite-resurs.</span><span class="sxs-lookup"><span data-stu-id="684e2-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="684e2-114">Det här är en RM-representation av kund grenar som laddas upp till Azure för S2S-anslutning med en cortex virtuellt hubb.</span><span class="sxs-lookup"><span data-stu-id="684e2-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="684e2-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="684e2-115">EXAMPLES</span></span>

### <span data-ttu-id="684e2-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="684e2-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "nonlinkSite"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "nonlinkSite" -Name myVirtualWAN -Location "East US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzVpnSite -ResourceGroupName "nonlinkSite" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : nonlinkSite
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="684e2-117">Ovanstående skapar en resurs grupp, virtuella WAN i öst-USA i resurs gruppen "nonlinkSite" i Azure.</span><span class="sxs-lookup"><span data-stu-id="684e2-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="684e2-118">Därefter skapas en VpnSite för att representera en kund gren och länkar den till den virtuella WAN-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="684e2-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="684e2-119">En IPSec-anslutning kan sedan installeras med den här grenen och en VpnGateway med kommandot New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="684e2-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="684e2-120">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="684e2-120">Example 2</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "multilink"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName multilink -Name myVirtualWAN -Location "East US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSiteLink2 = New-AzVpnSiteLink -Name "testVpnSiteLink2" -IpAddress "15.25.35.55" -LinkProviderName "SomeTelecomProvider2" -LinkSpeedInMbps "100"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "multilink" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink1, $vpnSiteLink2)
```

<span data-ttu-id="684e2-121">Ovanstående skapar en resurs grupp, en virtuell WAN-och en VpnSite med 1 VpnSiteLinks i öst-resurs gruppen "Multilink" i Azure.</span><span class="sxs-lookup"><span data-stu-id="684e2-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

### <span data-ttu-id="684e2-122">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="684e2-122">Example 3</span></span>

<span data-ttu-id="684e2-123">Skapar en ny Azure VpnSite-resurs.</span><span class="sxs-lookup"><span data-stu-id="684e2-123">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="684e2-124">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="684e2-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnSite -AddressSpace <String[]> -DeviceModel 'SomeDevice' -DeviceVendor 'SomeDeviceVendor' -IpAddress '1.2.3.4' -LinkSpeedInMbps '10' -Location 'East US' -Name 'testVpnSite' -ResourceGroupName 'multilink' -VirtualWanName <String> -VirtualWanResourceGroupName <String>
```

## <span data-ttu-id="684e2-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="684e2-125">PARAMETERS</span></span>

### <span data-ttu-id="684e2-126">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="684e2-126">-AddressSpace</span></span>
<span data-ttu-id="684e2-127">Adressprefix för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="684e2-127">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="684e2-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="684e2-128">-AsJob</span></span>
<span data-ttu-id="684e2-129">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="684e2-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="684e2-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="684e2-130">-BgpAsn</span></span>
<span data-ttu-id="684e2-131">BGP ASN för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="684e2-131">The BGP ASN for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684e2-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="684e2-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="684e2-133">BGP peering-adressen för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="684e2-133">The BGP Peering Address for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684e2-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="684e2-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="684e2-135">BGP-peering-vikten för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="684e2-135">The BGP Peering weight for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684e2-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="684e2-136">-DefaultProfile</span></span>
<span data-ttu-id="684e2-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="684e2-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="684e2-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="684e2-138">-DeviceModel</span></span>
<span data-ttu-id="684e2-139">Enhets modellen för fjärr-VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="684e2-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="684e2-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="684e2-140">-DeviceVendor</span></span>
<span data-ttu-id="684e2-141">Enhets leverantören för fjärr-VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="684e2-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="684e2-142">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="684e2-142">-IpAddress</span></span>
<span data-ttu-id="684e2-143">IPAddress för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="684e2-143">The IPAddress for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684e2-144">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="684e2-144">-LinkSpeedInMbps</span></span>
<span data-ttu-id="684e2-145">Enhets modellen för fjärr-VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="684e2-145">The device model of the remote vpn device.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684e2-146">-Plats</span><span class="sxs-lookup"><span data-stu-id="684e2-146">-Location</span></span>
<span data-ttu-id="684e2-147">Resurs platsen.</span><span class="sxs-lookup"><span data-stu-id="684e2-147">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684e2-148">-Namn</span><span class="sxs-lookup"><span data-stu-id="684e2-148">-Name</span></span>
<span data-ttu-id="684e2-149">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="684e2-149">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684e2-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="684e2-150">-O365Policy</span></span>
<span data-ttu-id="684e2-151">Översikten policy för Office 365 för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="684e2-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="684e2-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="684e2-152">-ResourceGroupName</span></span>
<span data-ttu-id="684e2-153">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="684e2-153">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684e2-154">-Tagg</span><span class="sxs-lookup"><span data-stu-id="684e2-154">-Tag</span></span>
<span data-ttu-id="684e2-155">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="684e2-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="684e2-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="684e2-156">-VirtualWan</span></span>
<span data-ttu-id="684e2-157">VirtualWan denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="684e2-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684e2-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="684e2-158">-VirtualWanId</span></span>
<span data-ttu-id="684e2-159">ResourceId-VirtualWan som denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="684e2-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684e2-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="684e2-160">-VirtualWanName</span></span>
<span data-ttu-id="684e2-161">Namnet på den VirtualWan som denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="684e2-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684e2-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="684e2-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="684e2-163">Namnet på den VirtualWan som denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="684e2-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684e2-164">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="684e2-164">-VpnSiteLink</span></span>
<span data-ttu-id="684e2-165">Listan med VpnSiteLinks som denna VpnSite har.</span><span class="sxs-lookup"><span data-stu-id="684e2-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: ByVirtualWanNameByVpnSiteLinkObject, ByVirtualWanObjectByVpnSiteLinkObject, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684e2-166">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="684e2-166">-Confirm</span></span>
<span data-ttu-id="684e2-167">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="684e2-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="684e2-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="684e2-168">-WhatIf</span></span>
<span data-ttu-id="684e2-169">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="684e2-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="684e2-170">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="684e2-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="684e2-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="684e2-171">CommonParameters</span></span>
<span data-ttu-id="684e2-172">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="684e2-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="684e2-173">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="684e2-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="684e2-174">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="684e2-174">INPUTS</span></span>

### <span data-ttu-id="684e2-175">Ingen</span><span class="sxs-lookup"><span data-stu-id="684e2-175">None</span></span>

## <span data-ttu-id="684e2-176">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="684e2-176">OUTPUTS</span></span>

### <span data-ttu-id="684e2-177">Microsoft. Azure. commands. Networks. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="684e2-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="684e2-178">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="684e2-178">NOTES</span></span>

## <span data-ttu-id="684e2-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="684e2-179">RELATED LINKS</span></span>

[<span data-ttu-id="684e2-180">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="684e2-180">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="684e2-181">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="684e2-181">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="684e2-182">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="684e2-182">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)