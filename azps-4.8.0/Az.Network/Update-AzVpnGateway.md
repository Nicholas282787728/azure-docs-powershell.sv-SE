---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: 419c7bc71def03bc2db004e378d80ea9c31f5183
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261775"
---
# <span data-ttu-id="d98a0-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d98a0-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="d98a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d98a0-102">SYNOPSIS</span></span>
<span data-ttu-id="d98a0-103">Uppdaterar en skalbar VPN-gateway.</span><span class="sxs-lookup"><span data-stu-id="d98a0-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="d98a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d98a0-104">SYNTAX</span></span>

### <span data-ttu-id="d98a0-105">ByVpnGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="d98a0-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d98a0-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="d98a0-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d98a0-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="d98a0-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d98a0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d98a0-108">DESCRIPTION</span></span>
<span data-ttu-id="d98a0-109">Cmdleten **Update-AzVpnGateway** uppdaterar en skalbar VPN-gateway.</span><span class="sxs-lookup"><span data-stu-id="d98a0-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="d98a0-110">En Azure VPN gateway är en program varu anslutning för webbplatsen till plats anslutningar i VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="d98a0-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="d98a0-111">Denna gateway ändrar storlek på och skalar baserat på den enhet som anges av användaren.</span><span class="sxs-lookup"><span data-stu-id="d98a0-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="d98a0-112">En anslutning kan konfigureras från en filial/webbplats som kallas VPN-plats till den utbyggbara gatewayen.</span><span class="sxs-lookup"><span data-stu-id="d98a0-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="d98a0-113">Varje anslutning består av 2 Active-Active tunnlar</span><span class="sxs-lookup"><span data-stu-id="d98a0-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="d98a0-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d98a0-114">EXAMPLES</span></span>

### <span data-ttu-id="d98a0-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d98a0-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="d98a0-116">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="d98a0-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="d98a0-117">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="d98a0-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="d98a0-118">När du har skapat gatewayen använder den Update-AzVpnGateway för att uppgradera gatewayen till 3 skal enheter.</span><span class="sxs-lookup"><span data-stu-id="d98a0-118">After the gateway has been created, it uses  Update-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

### <span data-ttu-id="d98a0-119">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d98a0-119">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\>$ipconfigurationId1 = 'Instance0'
PS C:\>$addresslist1 = @('169.254.21.5')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>$ipconfigurationId2 = 'Instance1'
PS C:\>$addresslist2 = @('169.254.21.10')
PS C:\>$gw1ipconfBgp2 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId2 -CustomAddress $addresslist2
PS C:\>$gw = Get-AzVpnGateway -ResourceGroupName testRg -Name testgw
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -BgpPeeringAddress @($gw1ipconfBgp1,$gw1ipconfBgp2)

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="d98a0-120">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="d98a0-120">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="d98a0-121">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="d98a0-121">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="d98a0-122">När du har skapat gatewayen använder den Set-AzVpnGateway för att uppdatera BgpPeeringAddress.</span><span class="sxs-lookup"><span data-stu-id="d98a0-122">After the gateway has been created, it uses Set-AzVpnGateway to update BgpPeeringAddress.</span></span>

## <span data-ttu-id="d98a0-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d98a0-123">PARAMETERS</span></span>

### <span data-ttu-id="d98a0-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d98a0-124">-AsJob</span></span>
<span data-ttu-id="d98a0-125">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d98a0-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d98a0-126">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="d98a0-126">-BgpPeeringAddress</span></span>
<span data-ttu-id="d98a0-127">BGP peering-adresser för den här VpnGateway bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="d98a0-127">The BGP peering addresses for this VpnGateway bgpsettings.</span></span>

```yaml
Type: PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d98a0-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d98a0-128">-Confirm</span></span>
<span data-ttu-id="d98a0-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d98a0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d98a0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d98a0-130">-DefaultProfile</span></span>
<span data-ttu-id="d98a0-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d98a0-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d98a0-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d98a0-132">-InputObject</span></span>
<span data-ttu-id="d98a0-133">VPN gateway-objekt som ska ändras</span><span class="sxs-lookup"><span data-stu-id="d98a0-133">The vpn gateway object to be modified</span></span>

```yaml
Type: PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d98a0-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="d98a0-134">-Name</span></span>
<span data-ttu-id="d98a0-135">VPN gateway-namnet.</span><span class="sxs-lookup"><span data-stu-id="d98a0-135">The vpn gateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d98a0-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d98a0-136">-ResourceGroupName</span></span>
<span data-ttu-id="d98a0-137">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="d98a0-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d98a0-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d98a0-138">-ResourceId</span></span>
<span data-ttu-id="d98a0-139">Azure-resurs-ID för VpnGateway som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="d98a0-139">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d98a0-140">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d98a0-140">-Tag</span></span>
<span data-ttu-id="d98a0-141">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="d98a0-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d98a0-142">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d98a0-142">-VpnConnection</span></span>
<span data-ttu-id="d98a0-143">Listan med VpnConnections som den här VpnGateway måste ha.</span><span class="sxs-lookup"><span data-stu-id="d98a0-143">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d98a0-144">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="d98a0-144">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="d98a0-145">Skalan för denna VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d98a0-145">The scale unit for this VpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d98a0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d98a0-146">-WhatIf</span></span>
<span data-ttu-id="d98a0-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d98a0-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d98a0-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d98a0-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d98a0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d98a0-149">CommonParameters</span></span>
<span data-ttu-id="d98a0-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d98a0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d98a0-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d98a0-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d98a0-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d98a0-152">INPUTS</span></span>

### <span data-ttu-id="d98a0-153">Microsoft. Azure. commands. Networks. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d98a0-153">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="d98a0-154">System. String</span><span class="sxs-lookup"><span data-stu-id="d98a0-154">System.String</span></span>

## <span data-ttu-id="d98a0-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d98a0-155">OUTPUTS</span></span>

### <span data-ttu-id="d98a0-156">Microsoft. Azure. commands. Networks. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d98a0-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="d98a0-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d98a0-157">NOTES</span></span>

## <span data-ttu-id="d98a0-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d98a0-158">RELATED LINKS</span></span>
[<span data-ttu-id="d98a0-159">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d98a0-159">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="d98a0-160">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d98a0-160">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="d98a0-161">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d98a0-161">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)