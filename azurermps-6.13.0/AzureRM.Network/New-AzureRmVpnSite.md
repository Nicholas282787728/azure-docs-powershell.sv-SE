---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnSite.md
ms.openlocfilehash: b8594aab0b9475ed37a0a205010e92fdb2a4db7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755538"
---
# <span data-ttu-id="ab04a-101">New-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="ab04a-101">New-AzureRmVpnSite</span></span>

## <span data-ttu-id="ab04a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab04a-102">SYNOPSIS</span></span>
<span data-ttu-id="ab04a-103">Skapar en ny Azure VpnSite-resurs.</span><span class="sxs-lookup"><span data-stu-id="ab04a-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="ab04a-104">Det här är en RM-representation av kund grenar som laddas upp till Azure för S2S-anslutning med en cortex virtuellt hubb.</span><span class="sxs-lookup"><span data-stu-id="ab04a-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab04a-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab04a-105">SYNTAX</span></span>

### <span data-ttu-id="ab04a-106">ByVirtualWanName (standard)</span><span class="sxs-lookup"><span data-stu-id="ab04a-106">ByVirtualWanName (Default)</span></span>
```
New-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab04a-107">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="ab04a-107">ByVirtualWanObject</span></span>
```
New-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab04a-108">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="ab04a-108">ByVirtualWanResourceId</span></span>
```
New-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab04a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab04a-109">DESCRIPTION</span></span>
<span data-ttu-id="ab04a-110">Skapar en ny Azure VpnSite-resurs.</span><span class="sxs-lookup"><span data-stu-id="ab04a-110">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="ab04a-111">Det här är en RM-representation av kund grenar som laddas upp till Azure för S2S-anslutning med en cortex virtuellt hubb.</span><span class="sxs-lookup"><span data-stu-id="ab04a-111">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="ab04a-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab04a-112">EXAMPLES</span></span>

### <span data-ttu-id="ab04a-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ab04a-113">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="ab04a-114">Ovanstående skapar en resurs grupp, virtuellt WAN i West-resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="ab04a-114">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="ab04a-115">Därefter skapas en VpnSite för att representera en kund gren och länkar den till den virtuella WAN-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ab04a-115">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="ab04a-116">En IPSec-anslutning kan sedan installeras med den här grenen och en VpnGateway med kommandot New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="ab04a-116">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzureRmVpnConnection command.</span></span>

## <span data-ttu-id="ab04a-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab04a-117">PARAMETERS</span></span>

### <span data-ttu-id="ab04a-118">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="ab04a-118">-AddressSpace</span></span>
<span data-ttu-id="ab04a-119">Adressprefix för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="ab04a-119">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="ab04a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab04a-120">-AsJob</span></span>
<span data-ttu-id="ab04a-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ab04a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab04a-122">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="ab04a-122">-BgpAsn</span></span>
<span data-ttu-id="ab04a-123">BGP ASN för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="ab04a-123">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="ab04a-124">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="ab04a-124">-BgpPeeringAddress</span></span>
<span data-ttu-id="ab04a-125">BGP peering-adressen för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="ab04a-125">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="ab04a-126">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="ab04a-126">-BgpPeeringWeight</span></span>
<span data-ttu-id="ab04a-127">BGP-peering-vikten för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="ab04a-127">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="ab04a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab04a-128">-DefaultProfile</span></span>
<span data-ttu-id="ab04a-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ab04a-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab04a-130">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="ab04a-130">-DeviceModel</span></span>
<span data-ttu-id="ab04a-131">Enhets modellen för fjärr-VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="ab04a-131">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="ab04a-132">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="ab04a-132">-DeviceVendor</span></span>
<span data-ttu-id="ab04a-133">Enhets leverantören för fjärr-VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="ab04a-133">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="ab04a-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="ab04a-134">-IpAddress</span></span>
<span data-ttu-id="ab04a-135">IPAddress för denna VpnSite.</span><span class="sxs-lookup"><span data-stu-id="ab04a-135">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="ab04a-136">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="ab04a-136">-LinkSpeedInMbps</span></span>
<span data-ttu-id="ab04a-137">Enhets modellen för fjärr-VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="ab04a-137">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="ab04a-138">-Plats</span><span class="sxs-lookup"><span data-stu-id="ab04a-138">-Location</span></span>
<span data-ttu-id="ab04a-139">Resurs platsen.</span><span class="sxs-lookup"><span data-stu-id="ab04a-139">The resource location.</span></span>

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

### <span data-ttu-id="ab04a-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="ab04a-140">-Name</span></span>
<span data-ttu-id="ab04a-141">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="ab04a-141">The resource name.</span></span>

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

### <span data-ttu-id="ab04a-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab04a-142">-ResourceGroupName</span></span>
<span data-ttu-id="ab04a-143">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="ab04a-143">The resource name.</span></span>

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

### <span data-ttu-id="ab04a-144">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ab04a-144">-Tag</span></span>
<span data-ttu-id="ab04a-145">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="ab04a-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ab04a-146">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="ab04a-146">-VirtualWan</span></span>
<span data-ttu-id="ab04a-147">VirtualWan denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="ab04a-147">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab04a-148">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="ab04a-148">-VirtualWanId</span></span>
<span data-ttu-id="ab04a-149">ResourceId-VirtualWan som denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="ab04a-149">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab04a-150">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="ab04a-150">-VirtualWanName</span></span>
<span data-ttu-id="ab04a-151">Namnet på den VirtualWan som denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="ab04a-151">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab04a-152">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab04a-152">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="ab04a-153">Namnet på den VirtualWan som denna VpnSite måste anslutas till.</span><span class="sxs-lookup"><span data-stu-id="ab04a-153">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab04a-154">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ab04a-154">-Confirm</span></span>
<span data-ttu-id="ab04a-155">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ab04a-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab04a-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab04a-156">-WhatIf</span></span>
<span data-ttu-id="ab04a-157">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ab04a-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab04a-158">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ab04a-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab04a-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab04a-159">CommonParameters</span></span>
<span data-ttu-id="ab04a-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab04a-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab04a-161">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab04a-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab04a-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab04a-162">INPUTS</span></span>

### <span data-ttu-id="ab04a-163">Ingen</span><span class="sxs-lookup"><span data-stu-id="ab04a-163">None</span></span>

## <span data-ttu-id="ab04a-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab04a-164">OUTPUTS</span></span>

### <span data-ttu-id="ab04a-165">Microsoft. Azure. commands. Networks. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="ab04a-165">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="ab04a-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab04a-166">NOTES</span></span>

## <span data-ttu-id="ab04a-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab04a-167">RELATED LINKS</span></span>
