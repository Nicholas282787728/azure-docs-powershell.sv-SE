---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualwanvpnconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWanVpnConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWanVpnConfiguration.md
ms.openlocfilehash: be0fbc9b9fc6d91a5bf94344f432b67dfc38cab3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576230"
---
# <span data-ttu-id="b644d-101">Get-AzureRmVirtualWanVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="b644d-101">Get-AzureRmVirtualWanVpnConfiguration</span></span>

## <span data-ttu-id="b644d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b644d-102">SYNOPSIS</span></span>
<span data-ttu-id="b644d-103">Hämtar VPN-konfigurationen för en delmängd av VpnSites som är ansluten till detta WAN via VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="b644d-103">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="b644d-104">Uppladdar den genererade VPN-konfigurationen till en lagrings-blob som anges av kunden.</span><span class="sxs-lookup"><span data-stu-id="b644d-104">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b644d-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b644d-105">SYNTAX</span></span>

### <span data-ttu-id="b644d-106">ByVirtualWanNameByVpnSiteObject (standard)</span><span class="sxs-lookup"><span data-stu-id="b644d-106">ByVirtualWanNameByVpnSiteObject (Default)</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b644d-107">ByVirtualWanNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="b644d-107">ByVirtualWanNameByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSiteId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b644d-108">ByVirtualWanObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="b644d-108">ByVirtualWanObjectByVpnSiteObject</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b644d-109">ByVirtualWanObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="b644d-109">ByVirtualWanObjectByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b644d-110">ByVirtualWanResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="b644d-110">ByVirtualWanResourceIdByVpnSiteObject</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b644d-111">ByVirtualWanResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="b644d-111">ByVirtualWanResourceIdByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b644d-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b644d-112">DESCRIPTION</span></span>
<span data-ttu-id="b644d-113">Hämtar VPN-konfigurationen för en delmängd av VpnSites som är ansluten till detta WAN via VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="b644d-113">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="b644d-114">Uppladdar den genererade VPN-konfigurationen till en lagrings-blob som anges av kunden.</span><span class="sxs-lookup"><span data-stu-id="b644d-114">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="b644d-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b644d-115">EXAMPLES</span></span>

### <span data-ttu-id="b644d-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b644d-116">Example 1</span></span>
```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite

PS C:\> $vpnSitesForConfig = New-Object Microsoft.Azure.Commands.Network.Models.PSVpnSite[] 1
PS C:\> $vpnSitesForConfig[0] = $vpnSite
PS C:\> Get-AzureRmVirtualWanVpnConfiguration -VirtualWan $virtualWan -StorageSasUrl "SignedSasUrl" -VpnSite $vpnSitesForConfig

SasUrl
------
SignedSasUrl
```

<span data-ttu-id="b644d-117">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en VpnSite i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="b644d-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="b644d-118">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="b644d-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="b644d-119">När gatewayen har skapats är den ansluten till VpnSite med kommandot New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="b644d-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="b644d-120">Konfigurationen hämtas då med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b644d-120">The configuration is then downloaded using this commandlet.</span></span>

<span data-ttu-id="b644d-121">Om cmdleten lyckas skrivs nedladdnings konfigurationen till den blob som anges av SignedSasUrl.</span><span class="sxs-lookup"><span data-stu-id="b644d-121">If the commandlet is successful, then the download configuration will be written to the blob indicated by the SignedSasUrl.</span></span>

## <span data-ttu-id="b644d-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b644d-122">PARAMETERS</span></span>

### <span data-ttu-id="b644d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b644d-123">-DefaultProfile</span></span>
<span data-ttu-id="b644d-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b644d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b644d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b644d-125">-InputObject</span></span>
<span data-ttu-id="b644d-126">VPN-objektet som ska ändras</span><span class="sxs-lookup"><span data-stu-id="b644d-126">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteObject, ByVirtualWanObjectByVpnSiteResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b644d-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="b644d-127">-Name</span></span>
<span data-ttu-id="b644d-128">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="b644d-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b644d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b644d-129">-ResourceGroupName</span></span>
<span data-ttu-id="b644d-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b644d-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b644d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b644d-131">-ResourceId</span></span>
<span data-ttu-id="b644d-132">Azure Resource ID för den virtuella WAN-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b644d-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b644d-133">-StorageSasUrl</span><span class="sxs-lookup"><span data-stu-id="b644d-133">-StorageSasUrl</span></span>
<span data-ttu-id="b644d-134">SAS URL för lagrings platsen där konfigurationen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="b644d-134">The SAS Url for the storage location where the configuration is to be generated.</span></span>

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

### <span data-ttu-id="b644d-135">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="b644d-135">-VpnSite</span></span>
<span data-ttu-id="b644d-136">Listan med VpnSite resurs-ID: n som konfigurerar konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="b644d-136">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite[]
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanObjectByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b644d-137">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="b644d-137">-VpnSiteId</span></span>
<span data-ttu-id="b644d-138">Listan med VpnSite resurs-ID: n som konfigurerar konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="b644d-138">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVirtualWanNameByVpnSiteResourceId, ByVirtualWanObjectByVpnSiteResourceId, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b644d-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b644d-139">-Confirm</span></span>
<span data-ttu-id="b644d-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b644d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b644d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b644d-141">-WhatIf</span></span>
<span data-ttu-id="b644d-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b644d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b644d-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b644d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b644d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b644d-144">CommonParameters</span></span>
<span data-ttu-id="b644d-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b644d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b644d-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b644d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b644d-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b644d-147">INPUTS</span></span>

### <span data-ttu-id="b644d-148">Microsoft. Azure. commands. Networks. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b644d-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="b644d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b644d-149">System.String</span></span>

## <span data-ttu-id="b644d-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b644d-150">OUTPUTS</span></span>

### <span data-ttu-id="b644d-151">Microsoft. Azure. commands. Networks. Models. PSVirtualWanVpnSitesConfiguration</span><span class="sxs-lookup"><span data-stu-id="b644d-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span></span>

## <span data-ttu-id="b644d-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b644d-152">NOTES</span></span>

## <span data-ttu-id="b644d-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b644d-153">RELATED LINKS</span></span>
