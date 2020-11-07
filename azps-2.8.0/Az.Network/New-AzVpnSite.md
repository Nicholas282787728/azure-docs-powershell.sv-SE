---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: fe9449eedaedfa08880548ceda769835d6eb3f7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919063"
---
# <span data-ttu-id="04a13-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="04a13-101">New-AzVpnSite</span></span>

## <span data-ttu-id="04a13-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04a13-102">SYNOPSIS</span></span>
<span data-ttu-id="04a13-103">Skapar en ny Azure VpnSite-resurs.</span><span class="sxs-lookup"><span data-stu-id="04a13-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="04a13-104">Det här är en RM-representation av kund grenar som laddas upp till Azure för S2S-anslutning med en cortex virtuellt hubb.</span><span class="sxs-lookup"><span data-stu-id="04a13-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="04a13-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04a13-105">SYNTAX</span></span>

### <span data-ttu-id="04a13-106">ByVirtualWanNameByVpnSiteIpAddress (standard)</span><span class="sxs-lookup"><span data-stu-id="04a13-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04a13-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="04a13-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04a13-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="04a13-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04a13-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="04a13-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04a13-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="04a13-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04a13-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="04a13-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="04a13-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04a13-112">DESCRIPTION</span></span>
<span data-ttu-id="04a13-113">Skapar en ny Azure VpnSite-resurs.</span><span class="sxs-lookup"><span data-stu-id="04a13-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="04a13-114">Det här är en RM-representation av kund grenar som laddas upp till Azure för S2S-anslutning med en cortex virtuellt hubb.</span><span class="sxs-lookup"><span data-stu-id="04a13-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="04a13-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04a13-115">EXAMPLES</span></span>

### <span data-ttu-id="04a13-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="04a13-116">Example 1</span></span>

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

<span data-ttu-id="04a13-117">Ovanstående skapar en resurs grupp, virtuella WAN i öst-USA i resurs gruppen "nonlinkSite" i Azure.</span><span class="sxs-lookup"><span data-stu-id="04a13-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="04a13-118">Därefter skapas en VpnSite för att representera en kund gren och länkar den till den virtuella WAN-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="04a13-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="04a13-119">En IPSec-anslutning kan sedan installeras med den här grenen och en VpnGateway med kommandot New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="04a13-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="04a13-120">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="04a13-120">Example 2</span></span>
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

<span data-ttu-id="04a13-121">Ovanstående skapar en resurs grupp, en virtuell WAN-och en VpnSite med 1 VpnSiteLinks i öst-resurs gruppen "Multilink" i Azure.</span><span class="sxs-lookup"><span data-stu-id="04a13-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

## <span data-ttu-id="04a13-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04a13-122">PARAMETERS</span></span>

### <span data-ttu-id="04a13-123">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="04a13-123">-AddressSpace</span></span>
<span data-ttu-id="04a13-124">Adressprefix för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="04a13-124">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="04a13-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04a13-125">-AsJob</span></span>
<span data-ttu-id="04a13-126">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="04a13-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04a13-127">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="04a13-127">-BgpAsn</span></span>
<span data-ttu-id="04a13-128">BGP ASN för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="04a13-128">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="04a13-129">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="04a13-129">-BgpPeeringAddress</span></span>
<span data-ttu-id="04a13-130">BGP peering-adressen för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="04a13-130">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="04a13-131">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="04a13-131">-BgpPeeringWeight</span></span>
<span data-ttu-id="04a13-132">BGP-peering-vikten för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="04a13-132">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="04a13-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04a13-133">-DefaultProfile</span></span>
<span data-ttu-id="04a13-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="04a13-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04a13-135">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="04a13-135">-DeviceModel</span></span>
<span data-ttu-id="04a13-136">Enhets modellen för fjärr-VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="04a13-136">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="04a13-137">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="04a13-137">-DeviceVendor</span></span>
<span data-ttu-id="04a13-138">Enhets leverantören för fjärr-VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="04a13-138">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="04a13-139">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="04a13-139">-IpAddress</span></span>
<span data-ttu-id="04a13-140">IPAddress för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="04a13-140">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="04a13-141">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="04a13-141">-LinkSpeedInMbps</span></span>
<span data-ttu-id="04a13-142">Enhets modellen för fjärr-VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="04a13-142">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="04a13-143">-Plats</span><span class="sxs-lookup"><span data-stu-id="04a13-143">-Location</span></span>
<span data-ttu-id="04a13-144">Resurs platsen.</span><span class="sxs-lookup"><span data-stu-id="04a13-144">The resource location.</span></span>

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

### <span data-ttu-id="04a13-145">-Namn</span><span class="sxs-lookup"><span data-stu-id="04a13-145">-Name</span></span>
<span data-ttu-id="04a13-146">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="04a13-146">The resource name.</span></span>

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

### <span data-ttu-id="04a13-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04a13-147">-ResourceGroupName</span></span>
<span data-ttu-id="04a13-148">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="04a13-148">The resource name.</span></span>

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

### <span data-ttu-id="04a13-149">-Tagg</span><span class="sxs-lookup"><span data-stu-id="04a13-149">-Tag</span></span>
<span data-ttu-id="04a13-150">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="04a13-150">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="04a13-151">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="04a13-151">-VirtualWan</span></span>
<span data-ttu-id="04a13-152">VirtualWan denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="04a13-152">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="04a13-153">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="04a13-153">-VirtualWanId</span></span>
<span data-ttu-id="04a13-154">ResourceId-VirtualWan som denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="04a13-154">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="04a13-155">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="04a13-155">-VirtualWanName</span></span>
<span data-ttu-id="04a13-156">Namnet på den VirtualWan som denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="04a13-156">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="04a13-157">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04a13-157">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="04a13-158">Namnet på den VirtualWan som denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="04a13-158">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="04a13-159">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="04a13-159">-VpnSiteLink</span></span>
<span data-ttu-id="04a13-160">Listan med VpnSiteLinks som denna VpnSite har.</span><span class="sxs-lookup"><span data-stu-id="04a13-160">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="04a13-161">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="04a13-161">-Confirm</span></span>
<span data-ttu-id="04a13-162">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="04a13-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04a13-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04a13-163">-WhatIf</span></span>
<span data-ttu-id="04a13-164">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="04a13-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04a13-165">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="04a13-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04a13-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04a13-166">CommonParameters</span></span>
<span data-ttu-id="04a13-167">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04a13-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04a13-168">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04a13-168">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04a13-169">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04a13-169">INPUTS</span></span>

### <span data-ttu-id="04a13-170">Ingen</span><span class="sxs-lookup"><span data-stu-id="04a13-170">None</span></span>

## <span data-ttu-id="04a13-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04a13-171">OUTPUTS</span></span>

### <span data-ttu-id="04a13-172">Microsoft. Azure. commands. Networks. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="04a13-172">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="04a13-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04a13-173">NOTES</span></span>

## <span data-ttu-id="04a13-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04a13-174">RELATED LINKS</span></span>

[<span data-ttu-id="04a13-175">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="04a13-175">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="04a13-176">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="04a13-176">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="04a13-177">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="04a13-177">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
