---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: 7cc9dbe5c4727c283ead66e88b6c52c9c2fcd00e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089058"
---
# <span data-ttu-id="43ace-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="43ace-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="43ace-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="43ace-102">SYNOPSIS</span></span>
<span data-ttu-id="43ace-103">Uppdaterar en skalbar ExpressRoute-Gateway.</span><span class="sxs-lookup"><span data-stu-id="43ace-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="43ace-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="43ace-104">SYNTAX</span></span>

### <span data-ttu-id="43ace-105">ByExpressRouteGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="43ace-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 -MaxScaleUnits <UInt32> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43ace-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="43ace-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> -MinScaleUnits <UInt32> -MaxScaleUnits <UInt32>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43ace-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="43ace-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> -MinScaleUnits <UInt32> -MaxScaleUnits <UInt32>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43ace-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="43ace-108">DESCRIPTION</span></span>

<span data-ttu-id="43ace-109">Set-AzExpressRouteGateway uppdaterar skal enheter för ExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="43ace-109">Set-AzExpressRouteGateway updates the scale units for the ExpressRouteGateway</span></span>

## <span data-ttu-id="43ace-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="43ace-110">EXAMPLES</span></span>

### <span data-ttu-id="43ace-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="43ace-111">Example 1</span></span>

```powershell
PS C:\>Set-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan =Set-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub =Set-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\>New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\>Set-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -MinScaleUnits 3

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 3
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="43ace-112">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="43ace-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="43ace-113">En ExpressRoute gateway kommer att skapas därefter i det virtuella navet med 2 ombyggnads enheter, som sedan kommer att ändras till 3 enheter</span><span class="sxs-lookup"><span data-stu-id="43ace-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="43ace-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="43ace-114">PARAMETERS</span></span>

### <span data-ttu-id="43ace-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43ace-115">-AsJob</span></span>
<span data-ttu-id="43ace-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="43ace-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43ace-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43ace-117">-DefaultProfile</span></span>
<span data-ttu-id="43ace-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="43ace-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43ace-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43ace-119">-InputObject</span></span>
<span data-ttu-id="43ace-120">Det ExpressRouteGateway som måste uppdateras.</span><span class="sxs-lookup"><span data-stu-id="43ace-120">The ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43ace-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="43ace-121">-MaxScaleUnits</span></span>
<span data-ttu-id="43ace-122">Maximalt antal skal enheter för denna ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="43ace-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="43ace-123">Giltigt intervall > 2</span><span class="sxs-lookup"><span data-stu-id="43ace-123">Valid range > 2</span></span>

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

### <span data-ttu-id="43ace-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="43ace-124">-MinScaleUnits</span></span>
<span data-ttu-id="43ace-125">Det minsta antalet skal enheter för denna ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="43ace-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="43ace-126">Giltigt intervall > 2</span><span class="sxs-lookup"><span data-stu-id="43ace-126">Valid range > 2</span></span>

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

### <span data-ttu-id="43ace-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="43ace-127">-Name</span></span>
<span data-ttu-id="43ace-128">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="43ace-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ace-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43ace-129">-ResourceGroupName</span></span>
<span data-ttu-id="43ace-130">Namnet på ExpressRouteGateway som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="43ace-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ace-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43ace-131">-ResourceId</span></span>
<span data-ttu-id="43ace-132">ID för den ExpressRouteGateway som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="43ace-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ace-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="43ace-133">-Tag</span></span>
<span data-ttu-id="43ace-134">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="43ace-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="43ace-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="43ace-135">-Confirm</span></span>
<span data-ttu-id="43ace-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="43ace-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43ace-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43ace-137">-WhatIf</span></span>
<span data-ttu-id="43ace-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="43ace-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43ace-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="43ace-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43ace-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ace-140">CommonParameters</span></span>
<span data-ttu-id="43ace-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43ace-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ace-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43ace-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ace-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="43ace-143">INPUTS</span></span>

### <span data-ttu-id="43ace-144">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="43ace-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="43ace-145">System. String</span><span class="sxs-lookup"><span data-stu-id="43ace-145">System.String</span></span>

## <span data-ttu-id="43ace-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="43ace-146">OUTPUTS</span></span>

### <span data-ttu-id="43ace-147">Microsoft. Azure. commands. Networks. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="43ace-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="43ace-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="43ace-148">NOTES</span></span>

## <span data-ttu-id="43ace-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="43ace-149">RELATED LINKS</span></span>