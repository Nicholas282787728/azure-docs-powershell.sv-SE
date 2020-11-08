---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: 8db43fc826086235a51f32e67a8f787a3ac5792d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089497"
---
# <span data-ttu-id="ee14c-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ee14c-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="ee14c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee14c-102">SYNOPSIS</span></span>
<span data-ttu-id="ee14c-103">Uppdaterar en skalbar VPN-gateway.</span><span class="sxs-lookup"><span data-stu-id="ee14c-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="ee14c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee14c-104">SYNTAX</span></span>

### <span data-ttu-id="ee14c-105">ByVpnGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="ee14c-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee14c-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="ee14c-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee14c-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="ee14c-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee14c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee14c-108">DESCRIPTION</span></span>
<span data-ttu-id="ee14c-109">Cmdleten **Update-AzVpnGateway** uppdaterar en skalbar VPN-gateway.</span><span class="sxs-lookup"><span data-stu-id="ee14c-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="ee14c-110">En Azure VPN gateway är en program varu anslutning för webbplatsen till plats anslutningar i VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="ee14c-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="ee14c-111">Denna gateway ändrar storlek på och skalar baserat på den enhet som anges av användaren.</span><span class="sxs-lookup"><span data-stu-id="ee14c-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="ee14c-112">En anslutning kan konfigureras från en filial/webbplats som kallas VPN-plats till den utbyggbara gatewayen.</span><span class="sxs-lookup"><span data-stu-id="ee14c-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="ee14c-113">Varje anslutning består av 2 Active-Active tunnlar</span><span class="sxs-lookup"><span data-stu-id="ee14c-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="ee14c-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee14c-114">EXAMPLES</span></span>

### <span data-ttu-id="ee14c-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ee14c-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Set-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

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

<span data-ttu-id="ee14c-116">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="ee14c-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="ee14c-117">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="ee14c-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="ee14c-118">När du har skapat gatewayen använder den Set-AzVpnGateway för att uppgradera gatewayen till 3 skal enheter.</span><span class="sxs-lookup"><span data-stu-id="ee14c-118">After the gateway has been created, it uses Set-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

## <span data-ttu-id="ee14c-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee14c-119">PARAMETERS</span></span>

### <span data-ttu-id="ee14c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee14c-120">-AsJob</span></span>
<span data-ttu-id="ee14c-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ee14c-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee14c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee14c-122">-DefaultProfile</span></span>
<span data-ttu-id="ee14c-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ee14c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee14c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee14c-124">-InputObject</span></span>
<span data-ttu-id="ee14c-125">VPN gateway-objekt som ska ändras</span><span class="sxs-lookup"><span data-stu-id="ee14c-125">The vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee14c-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="ee14c-126">-Name</span></span>
<span data-ttu-id="ee14c-127">Virtuellt WAN-namn.</span><span class="sxs-lookup"><span data-stu-id="ee14c-127">The virtual wan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee14c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee14c-128">-ResourceGroupName</span></span>
<span data-ttu-id="ee14c-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ee14c-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee14c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee14c-130">-ResourceId</span></span>
<span data-ttu-id="ee14c-131">Azure-resurs-ID för VpnGateway som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="ee14c-131">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee14c-132">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ee14c-132">-Tag</span></span>
<span data-ttu-id="ee14c-133">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="ee14c-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ee14c-134">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ee14c-134">-VpnConnection</span></span>
<span data-ttu-id="ee14c-135">Listan med VpnConnections som den här VpnGateway måste ha.</span><span class="sxs-lookup"><span data-stu-id="ee14c-135">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee14c-136">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="ee14c-136">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="ee14c-137">Skalan för denna VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="ee14c-137">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="ee14c-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ee14c-138">-Confirm</span></span>
<span data-ttu-id="ee14c-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ee14c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee14c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee14c-140">-WhatIf</span></span>
<span data-ttu-id="ee14c-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ee14c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee14c-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ee14c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee14c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee14c-143">CommonParameters</span></span>
<span data-ttu-id="ee14c-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee14c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee14c-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee14c-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee14c-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee14c-146">INPUTS</span></span>

### <span data-ttu-id="ee14c-147">Microsoft. Azure. commands. Networks. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ee14c-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="ee14c-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ee14c-148">System.String</span></span>

## <span data-ttu-id="ee14c-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee14c-149">OUTPUTS</span></span>

### <span data-ttu-id="ee14c-150">Microsoft. Azure. commands. Networks. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ee14c-150">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="ee14c-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee14c-151">NOTES</span></span>

## <span data-ttu-id="ee14c-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee14c-152">RELATED LINKS</span></span>

[<span data-ttu-id="ee14c-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ee14c-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="ee14c-154">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ee14c-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="ee14c-155">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ee14c-155">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)
