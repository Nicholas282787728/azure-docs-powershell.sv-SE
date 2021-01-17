---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: fa7374264e46e65dcddacb9f35e5822f18294147
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401224"
---
# <span data-ttu-id="c0810-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c0810-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="c0810-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0810-102">SYNOPSIS</span></span>
<span data-ttu-id="c0810-103">Skapar en skalbar VPN-gateway.</span><span class="sxs-lookup"><span data-stu-id="c0810-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="c0810-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0810-104">SYNTAX</span></span>

### <span data-ttu-id="c0810-105">ByVirtualHubName (standard)</span><span class="sxs-lookup"><span data-stu-id="c0810-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0810-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="c0810-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0810-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="c0810-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0810-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0810-108">DESCRIPTION</span></span>

<span data-ttu-id="c0810-109">New-AzVpnGateway skapar en skalbar VPN-gateway.</span><span class="sxs-lookup"><span data-stu-id="c0810-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span> <span data-ttu-id="c0810-110">Det här är program varu definierad anslutning för webbplatsen till plats anslutningar i VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="c0810-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span> 

<span data-ttu-id="c0810-111">Denna gateway ändrar storlek på och skalar baserat på den enhet som anges i denna eller Set-AzVpnGateway cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0810-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span> 

<span data-ttu-id="c0810-112">En anslutning skapas från en filial/webbplats som kallas VPNSite till den utbyggbara gatewayen.</span><span class="sxs-lookup"><span data-stu-id="c0810-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="c0810-113">Varje anslutning består av 2 Active-Active tunnlar.</span><span class="sxs-lookup"><span data-stu-id="c0810-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="c0810-114">VpnGateway kommer att finnas på samma plats som refererade VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="c0810-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="c0810-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0810-115">EXAMPLES</span></span>

### <span data-ttu-id="c0810-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c0810-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="c0810-117">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="c0810-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="c0810-118">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="c0810-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="c0810-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0810-119">PARAMETERS</span></span>

### <span data-ttu-id="c0810-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0810-120">-AsJob</span></span>
<span data-ttu-id="c0810-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c0810-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0810-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0810-122">-DefaultProfile</span></span>
<span data-ttu-id="c0810-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0810-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0810-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="c0810-124">-Name</span></span>
<span data-ttu-id="c0810-125">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="c0810-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0810-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0810-126">-ResourceGroupName</span></span>
<span data-ttu-id="c0810-127">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="c0810-127">The resource name.</span></span>

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

### <span data-ttu-id="c0810-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c0810-128">-Tag</span></span>
<span data-ttu-id="c0810-129">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="c0810-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c0810-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="c0810-130">-VirtualHub</span></span>
<span data-ttu-id="c0810-131">VirtualHub som denna VpnGateway måste kopplas till.</span><span class="sxs-lookup"><span data-stu-id="c0810-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0810-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="c0810-132">-VirtualHubId</span></span>
<span data-ttu-id="c0810-133">ID för VirtualHub som denna VpnGateway måste kopplas till.</span><span class="sxs-lookup"><span data-stu-id="c0810-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0810-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="c0810-134">-VirtualHubName</span></span>
<span data-ttu-id="c0810-135">ID för VirtualHub som denna VpnGateway måste kopplas till.</span><span class="sxs-lookup"><span data-stu-id="c0810-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0810-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="c0810-136">-VpnConnection</span></span>
<span data-ttu-id="c0810-137">Listan med VpnConnections som den här VpnGateway måste ha.</span><span class="sxs-lookup"><span data-stu-id="c0810-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="c0810-138">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="c0810-138">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="c0810-139">Skalan för denna VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c0810-139">The scale unit for this VpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0810-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c0810-140">-Confirm</span></span>
<span data-ttu-id="c0810-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0810-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0810-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0810-142">-WhatIf</span></span>
<span data-ttu-id="c0810-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c0810-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0810-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c0810-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0810-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0810-145">CommonParameters</span></span>
<span data-ttu-id="c0810-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0810-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0810-147">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0810-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0810-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0810-148">INPUTS</span></span>

### <span data-ttu-id="c0810-149">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c0810-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="c0810-150">System. String</span><span class="sxs-lookup"><span data-stu-id="c0810-150">System.String</span></span>

## <span data-ttu-id="c0810-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0810-151">OUTPUTS</span></span>

### <span data-ttu-id="c0810-152">Microsoft. Azure. commands. Networks. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c0810-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="c0810-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0810-153">NOTES</span></span>

## <span data-ttu-id="c0810-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0810-154">RELATED LINKS</span></span>

[<span data-ttu-id="c0810-155">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c0810-155">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="c0810-156">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c0810-156">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="c0810-157">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c0810-157">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
