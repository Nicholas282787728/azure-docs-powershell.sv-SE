---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnGateway.md
ms.openlocfilehash: 00730f6e252373eebbbbc476fdd889b2eeb39e12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756142"
---
# <span data-ttu-id="5c8b4-101">Update-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="5c8b4-101">Update-AzureRmVpnGateway</span></span>

## <span data-ttu-id="5c8b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5c8b4-102">SYNOPSIS</span></span>
<span data-ttu-id="5c8b4-103">Update-AzureRmVpnGateway uppdaterar en skalbar VPN-gateway till rätt mål tillstånd.</span><span class="sxs-lookup"><span data-stu-id="5c8b4-103">Update-AzureRmVpnGateway updates a scalable VPN Gateway to the appropriate goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c8b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5c8b4-104">SYNTAX</span></span>

### <span data-ttu-id="5c8b4-105">ByVpnGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="5c8b4-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c8b4-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="5c8b4-106">ByVpnGatewayObject</span></span>
```
Update-AzureRmVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c8b4-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="5c8b4-107">ByVpnGatewayResourceId</span></span>
```
Update-AzureRmVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c8b4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5c8b4-108">DESCRIPTION</span></span>
<span data-ttu-id="5c8b4-109">Update-AzureRmVpnGateway uppdaterar en skalbar VPN-gateway till rätt mål tillstånd.</span><span class="sxs-lookup"><span data-stu-id="5c8b4-109">Update-AzureRmVpnGateway updates a scalable VPN Gateway to the appropriate goal state.</span></span> <span data-ttu-id="5c8b4-110">En AzureRmVpnGateway är en program varu anslutning för webbplats anslutningar i VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="5c8b4-110">An AzureRmVpnGateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="5c8b4-111">Denna gateway ändrar storlek på och skalar baserat på den enhet som anges av användaren.</span><span class="sxs-lookup"><span data-stu-id="5c8b4-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="5c8b4-112">Det går att konfigurera en anslutning från en filial/webbplats som kallas VPNSite till den utbyggbara gatewayen.</span><span class="sxs-lookup"><span data-stu-id="5c8b4-112">A connection can be set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="5c8b4-113">Varje anslutning består av 2 Active-Active tunnlar</span><span class="sxs-lookup"><span data-stu-id="5c8b4-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="5c8b4-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5c8b4-114">EXAMPLES</span></span>

### <span data-ttu-id="5c8b4-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5c8b4-115">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Set-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

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

<span data-ttu-id="5c8b4-116">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="5c8b4-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="5c8b4-117">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="5c8b4-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="5c8b4-118">När du har skapat gatewayen använder den Set-AzureRmVpnGateway för att uppgradera gatewayen till 3 skal enheter.</span><span class="sxs-lookup"><span data-stu-id="5c8b4-118">After the gateway has been created, it uses Set-AzureRmVpnGateway to upgrade the gateway to 3 scale units.</span></span>

## <span data-ttu-id="5c8b4-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5c8b4-119">PARAMETERS</span></span>

### <span data-ttu-id="5c8b4-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c8b4-120">-AsJob</span></span>
<span data-ttu-id="5c8b4-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5c8b4-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c8b4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c8b4-122">-DefaultProfile</span></span>
<span data-ttu-id="5c8b4-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5c8b4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c8b4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c8b4-124">-InputObject</span></span>
<span data-ttu-id="5c8b4-125">VPN gateway-objekt som ska ändras</span><span class="sxs-lookup"><span data-stu-id="5c8b4-125">The vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="5c8b4-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="5c8b4-126">-Name</span></span>
<span data-ttu-id="5c8b4-127">Virtuellt WAN-namn.</span><span class="sxs-lookup"><span data-stu-id="5c8b4-127">The virtual wan name.</span></span>

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

### <span data-ttu-id="5c8b4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c8b4-128">-ResourceGroupName</span></span>
<span data-ttu-id="5c8b4-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="5c8b4-129">The resource group name.</span></span>

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

### <span data-ttu-id="5c8b4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c8b4-130">-ResourceId</span></span>
<span data-ttu-id="5c8b4-131">Azure-resurs-ID för VpnGateway som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="5c8b4-131">The Azure resource ID of the VpnGateway to be modified.</span></span>

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

### <span data-ttu-id="5c8b4-132">-Tagg</span><span class="sxs-lookup"><span data-stu-id="5c8b4-132">-Tag</span></span>
<span data-ttu-id="5c8b4-133">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="5c8b4-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="5c8b4-134">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="5c8b4-134">-VpnConnection</span></span>
<span data-ttu-id="5c8b4-135">Listan med VpnConnections som den här VpnGateway måste ha.</span><span class="sxs-lookup"><span data-stu-id="5c8b4-135">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="5c8b4-136">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="5c8b4-136">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="5c8b4-137">Skalan för denna VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="5c8b4-137">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="5c8b4-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5c8b4-138">-Confirm</span></span>
<span data-ttu-id="5c8b4-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5c8b4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c8b4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c8b4-140">-WhatIf</span></span>
<span data-ttu-id="5c8b4-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5c8b4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c8b4-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5c8b4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c8b4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c8b4-143">CommonParameters</span></span>
<span data-ttu-id="5c8b4-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c8b4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c8b4-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c8b4-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c8b4-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5c8b4-146">INPUTS</span></span>

### <span data-ttu-id="5c8b4-147">Microsoft. Azure. commands. Networks. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="5c8b4-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="5c8b4-148">System. String</span><span class="sxs-lookup"><span data-stu-id="5c8b4-148">System.String</span></span>

## <span data-ttu-id="5c8b4-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5c8b4-149">OUTPUTS</span></span>

### <span data-ttu-id="5c8b4-150">Microsoft. Azure. commands. Networks. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="5c8b4-150">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="5c8b4-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5c8b4-151">NOTES</span></span>

## <span data-ttu-id="5c8b4-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5c8b4-152">RELATED LINKS</span></span>
