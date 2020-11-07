---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
ms.openlocfilehash: b0c04db4eccc784e7ae55bcabed09ed753081fa7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748185"
---
# <span data-ttu-id="f4268-101">Get-AzVirtualWanVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4268-101">Get-AzVirtualWanVpnConfiguration</span></span>

## <span data-ttu-id="f4268-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4268-102">SYNOPSIS</span></span>
<span data-ttu-id="f4268-103">Hämtar VPN-konfigurationen för en delmängd av VpnSites som är ansluten till detta WAN via VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="f4268-103">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="f4268-104">Uppladdar den genererade VPN-konfigurationen till en lagrings-blob som anges av kunden.</span><span class="sxs-lookup"><span data-stu-id="f4268-104">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="f4268-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4268-105">SYNTAX</span></span>

### <span data-ttu-id="f4268-106">ByVirtualWanNameByVpnSiteObject (standard)</span><span class="sxs-lookup"><span data-stu-id="f4268-106">ByVirtualWanNameByVpnSiteObject (Default)</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4268-107">ByVirtualWanNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="f4268-107">ByVirtualWanNameByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSiteId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4268-108">ByVirtualWanObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="f4268-108">ByVirtualWanObjectByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4268-109">ByVirtualWanObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="f4268-109">ByVirtualWanObjectByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4268-110">ByVirtualWanResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="f4268-110">ByVirtualWanResourceIdByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4268-111">ByVirtualWanResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="f4268-111">ByVirtualWanResourceIdByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4268-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4268-112">DESCRIPTION</span></span>
<span data-ttu-id="f4268-113">Hämtar VPN-konfigurationen för en delmängd av VpnSites som är ansluten till detta WAN via VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="f4268-113">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="f4268-114">Uppladdar den genererade VPN-konfigurationen till en lagrings-blob som anges av kunden.</span><span class="sxs-lookup"><span data-stu-id="f4268-114">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="f4268-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4268-115">EXAMPLES</span></span>

### <span data-ttu-id="f4268-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f4268-116">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite

PS C:\> $vpnSitesForConfig = New-Object Microsoft.Azure.Commands.Network.Models.PSVpnSite[] 1
PS C:\> $vpnSitesForConfig[0] = $vpnSite
PS C:\> Get-AzVirtualWanVpnConfiguration -VirtualWan $virtualWan -StorageSasUrl "SignedSasUrl" -VpnSite $vpnSitesForConfig

SasUrl
------
SignedSasUrl
```

<span data-ttu-id="f4268-117">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en VpnSite i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="f4268-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="f4268-118">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="f4268-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="f4268-119">När gatewayen har skapats är den ansluten till VpnSite med kommandot New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="f4268-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="f4268-120">Konfigurationen hämtas då med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f4268-120">The configuration is then downloaded using this commandlet.</span></span>

<span data-ttu-id="f4268-121">Om cmdleten lyckas skrivs nedladdnings konfigurationen till den blob som anges av SignedSasUrl.</span><span class="sxs-lookup"><span data-stu-id="f4268-121">If the commandlet is successful, then the download configuration will be written to the blob indicated by the SignedSasUrl.</span></span>

## <span data-ttu-id="f4268-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4268-122">PARAMETERS</span></span>

### <span data-ttu-id="f4268-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4268-123">-DefaultProfile</span></span>
<span data-ttu-id="f4268-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f4268-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4268-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4268-125">-InputObject</span></span>
<span data-ttu-id="f4268-126">VPN-objektet som ska ändras</span><span class="sxs-lookup"><span data-stu-id="f4268-126">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="f4268-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="f4268-127">-Name</span></span>
<span data-ttu-id="f4268-128">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="f4268-128">The resource name.</span></span>

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

### <span data-ttu-id="f4268-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4268-129">-ResourceGroupName</span></span>
<span data-ttu-id="f4268-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="f4268-130">The resource group name.</span></span>

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

### <span data-ttu-id="f4268-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4268-131">-ResourceId</span></span>
<span data-ttu-id="f4268-132">Azure Resource ID för den virtuella WAN-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f4268-132">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="f4268-133">-StorageSasUrl</span><span class="sxs-lookup"><span data-stu-id="f4268-133">-StorageSasUrl</span></span>
<span data-ttu-id="f4268-134">SAS URL för lagrings platsen där konfigurationen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="f4268-134">The SAS Url for the storage location where the configuration is to be generated.</span></span>

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

### <span data-ttu-id="f4268-135">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="f4268-135">-VpnSite</span></span>
<span data-ttu-id="f4268-136">Listan med VpnSite resurs-ID: n som konfigurerar konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="f4268-136">The list of VpnSite resource ids to generate configuration for.</span></span>

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

### <span data-ttu-id="f4268-137">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="f4268-137">-VpnSiteId</span></span>
<span data-ttu-id="f4268-138">Listan med VpnSite resurs-ID: n som konfigurerar konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="f4268-138">The list of VpnSite resource ids to generate configuration for.</span></span>

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

### <span data-ttu-id="f4268-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f4268-139">-Confirm</span></span>
<span data-ttu-id="f4268-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f4268-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4268-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4268-141">-WhatIf</span></span>
<span data-ttu-id="f4268-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f4268-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4268-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f4268-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4268-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4268-144">CommonParameters</span></span>
<span data-ttu-id="f4268-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4268-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4268-146">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4268-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4268-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4268-147">INPUTS</span></span>

### <span data-ttu-id="f4268-148">Microsoft. Azure. commands. Networks. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f4268-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="f4268-149">System. String</span><span class="sxs-lookup"><span data-stu-id="f4268-149">System.String</span></span>

## <span data-ttu-id="f4268-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4268-150">OUTPUTS</span></span>

### <span data-ttu-id="f4268-151">Microsoft. Azure. commands. Networks. Models. PSVirtualWanVpnSitesConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4268-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span></span>

## <span data-ttu-id="f4268-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4268-152">NOTES</span></span>

## <span data-ttu-id="f4268-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4268-153">RELATED LINKS</span></span>
