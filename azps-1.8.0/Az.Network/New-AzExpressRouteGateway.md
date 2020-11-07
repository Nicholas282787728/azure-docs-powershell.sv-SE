---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: 6aabba5154e14f3af0ccfff20569c0cdc51a2578
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748075"
---
# <span data-ttu-id="ec88d-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="ec88d-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="ec88d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ec88d-102">SYNOPSIS</span></span>
<span data-ttu-id="ec88d-103">Skapar en skalbar ExpressRoute Gateway.</span><span class="sxs-lookup"><span data-stu-id="ec88d-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="ec88d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ec88d-104">SYNTAX</span></span>

### <span data-ttu-id="ec88d-105">ByVirtualHubName (standard)</span><span class="sxs-lookup"><span data-stu-id="ec88d-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec88d-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="ec88d-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec88d-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="ec88d-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec88d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ec88d-108">DESCRIPTION</span></span>

<span data-ttu-id="ec88d-109">New-AzExpressRouteGateway skapar en skalbar Gateway för ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ec88d-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="ec88d-110">Det här är program varu definition som definierats för lokal kommunikation i Azure inuti VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="ec88d-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="ec88d-111">Denna gateway kan skalas baserat på den enhet som anges i denna eller Set-AzExpressRouteGateway cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec88d-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="ec88d-112">En anslutning är inställd från en lokal ExpressRoute-krets till den utbyggbara gatewayen.</span><span class="sxs-lookup"><span data-stu-id="ec88d-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="ec88d-113">ExpressRouteGateway kommer att finnas på samma plats som refererade VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="ec88d-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="ec88d-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ec88d-114">EXAMPLES</span></span>

### <span data-ttu-id="ec88d-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ec88d-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="ec88d-116">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="ec88d-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="ec88d-117">En ExpressRoute gateway kommer att skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="ec88d-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="ec88d-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ec88d-118">PARAMETERS</span></span>

### <span data-ttu-id="ec88d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec88d-119">-AsJob</span></span>
<span data-ttu-id="ec88d-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ec88d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec88d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec88d-121">-DefaultProfile</span></span>
<span data-ttu-id="ec88d-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ec88d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec88d-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="ec88d-123">-MaxScaleUnits</span></span>
<span data-ttu-id="ec88d-124">Maximalt antal skal enheter för denna ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="ec88d-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="ec88d-125">Giltigt intervall > 2</span><span class="sxs-lookup"><span data-stu-id="ec88d-125">Valid range > 2</span></span>

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

### <span data-ttu-id="ec88d-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="ec88d-126">-MinScaleUnits</span></span>
<span data-ttu-id="ec88d-127">Det minsta antalet skal enheter för denna ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="ec88d-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="ec88d-128">Giltigt intervall > 2</span><span class="sxs-lookup"><span data-stu-id="ec88d-128">Valid range > 2</span></span>

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

### <span data-ttu-id="ec88d-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="ec88d-129">-Name</span></span>
<span data-ttu-id="ec88d-130">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="ec88d-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec88d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec88d-131">-ResourceGroupName</span></span>
<span data-ttu-id="ec88d-132">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="ec88d-132">The resource name.</span></span>

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

### <span data-ttu-id="ec88d-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ec88d-133">-Tag</span></span>
<span data-ttu-id="ec88d-134">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="ec88d-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ec88d-135">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="ec88d-135">-VirtualHub</span></span>
<span data-ttu-id="ec88d-136">VirtualHub som denna VpnGateway måste kopplas till.</span><span class="sxs-lookup"><span data-stu-id="ec88d-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="ec88d-137">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="ec88d-137">-VirtualHubId</span></span>
<span data-ttu-id="ec88d-138">ID för VirtualHub som denna VpnGateway måste kopplas till.</span><span class="sxs-lookup"><span data-stu-id="ec88d-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="ec88d-139">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="ec88d-139">-VirtualHubName</span></span>
<span data-ttu-id="ec88d-140">ID för VirtualHub som denna VpnGateway måste kopplas till.</span><span class="sxs-lookup"><span data-stu-id="ec88d-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="ec88d-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ec88d-141">-Confirm</span></span>
<span data-ttu-id="ec88d-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ec88d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec88d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec88d-143">-WhatIf</span></span>
<span data-ttu-id="ec88d-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ec88d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec88d-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ec88d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec88d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec88d-146">CommonParameters</span></span>
<span data-ttu-id="ec88d-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec88d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec88d-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec88d-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec88d-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ec88d-149">INPUTS</span></span>

### <span data-ttu-id="ec88d-150">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ec88d-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="ec88d-151">System. String</span><span class="sxs-lookup"><span data-stu-id="ec88d-151">System.String</span></span>

## <span data-ttu-id="ec88d-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ec88d-152">OUTPUTS</span></span>

### <span data-ttu-id="ec88d-153">Microsoft. Azure. commands. Networks. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="ec88d-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="ec88d-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ec88d-154">NOTES</span></span>

## <span data-ttu-id="ec88d-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ec88d-155">RELATED LINKS</span></span>
