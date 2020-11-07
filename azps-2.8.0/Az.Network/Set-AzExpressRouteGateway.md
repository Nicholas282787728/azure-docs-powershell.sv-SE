---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: c3d311cc091026bcd08225e5a11a8232102a03a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918945"
---
# <span data-ttu-id="3b9d7-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="3b9d7-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="3b9d7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b9d7-102">SYNOPSIS</span></span>
<span data-ttu-id="3b9d7-103">Uppdaterar en skalbar ExpressRoute-Gateway.</span><span class="sxs-lookup"><span data-stu-id="3b9d7-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="3b9d7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b9d7-104">SYNTAX</span></span>

### <span data-ttu-id="3b9d7-105">ByExpressRouteGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="3b9d7-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 -MaxScaleUnits <UInt32> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b9d7-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="3b9d7-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> -MinScaleUnits <UInt32> -MaxScaleUnits <UInt32>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b9d7-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="3b9d7-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> -MinScaleUnits <UInt32> -MaxScaleUnits <UInt32>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b9d7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b9d7-108">DESCRIPTION</span></span>

<span data-ttu-id="3b9d7-109">Set-AzExpressRouteGateway uppdaterar skal enheter för ExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="3b9d7-109">Set-AzExpressRouteGateway updates the scale units for the ExpressRouteGateway</span></span>

## <span data-ttu-id="3b9d7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b9d7-110">EXAMPLES</span></span>

### <span data-ttu-id="3b9d7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3b9d7-111">Example 1</span></span>

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

<span data-ttu-id="3b9d7-112">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="3b9d7-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="3b9d7-113">En ExpressRoute gateway kommer att skapas därefter i det virtuella navet med 2 ombyggnads enheter, som sedan kommer att ändras till 3 enheter</span><span class="sxs-lookup"><span data-stu-id="3b9d7-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="3b9d7-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b9d7-114">PARAMETERS</span></span>

### <span data-ttu-id="3b9d7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b9d7-115">-AsJob</span></span>
<span data-ttu-id="3b9d7-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3b9d7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b9d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b9d7-117">-DefaultProfile</span></span>
<span data-ttu-id="3b9d7-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3b9d7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b9d7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b9d7-119">-InputObject</span></span>
<span data-ttu-id="3b9d7-120">Det ExpressRouteGateway som måste uppdateras.</span><span class="sxs-lookup"><span data-stu-id="3b9d7-120">The ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="3b9d7-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="3b9d7-121">-MaxScaleUnits</span></span>
<span data-ttu-id="3b9d7-122">Maximalt antal skal enheter för denna ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="3b9d7-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="3b9d7-123">Giltigt intervall > 2</span><span class="sxs-lookup"><span data-stu-id="3b9d7-123">Valid range > 2</span></span>

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

### <span data-ttu-id="3b9d7-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="3b9d7-124">-MinScaleUnits</span></span>
<span data-ttu-id="3b9d7-125">Det minsta antalet skal enheter för denna ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="3b9d7-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="3b9d7-126">Giltigt intervall > 2</span><span class="sxs-lookup"><span data-stu-id="3b9d7-126">Valid range > 2</span></span>

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

### <span data-ttu-id="3b9d7-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="3b9d7-127">-Name</span></span>
<span data-ttu-id="3b9d7-128">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="3b9d7-128">The resource name.</span></span>

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

### <span data-ttu-id="3b9d7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b9d7-129">-ResourceGroupName</span></span>
<span data-ttu-id="3b9d7-130">Namnet på ExpressRouteGateway som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="3b9d7-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

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

### <span data-ttu-id="3b9d7-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b9d7-131">-ResourceId</span></span>
<span data-ttu-id="3b9d7-132">ID för den ExpressRouteGateway som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="3b9d7-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="3b9d7-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3b9d7-133">-Tag</span></span>
<span data-ttu-id="3b9d7-134">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="3b9d7-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3b9d7-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3b9d7-135">-Confirm</span></span>
<span data-ttu-id="3b9d7-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3b9d7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b9d7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b9d7-137">-WhatIf</span></span>
<span data-ttu-id="3b9d7-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3b9d7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b9d7-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3b9d7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b9d7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b9d7-140">CommonParameters</span></span>
<span data-ttu-id="3b9d7-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b9d7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b9d7-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b9d7-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b9d7-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b9d7-143">INPUTS</span></span>

### <span data-ttu-id="3b9d7-144">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3b9d7-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="3b9d7-145">System. String</span><span class="sxs-lookup"><span data-stu-id="3b9d7-145">System.String</span></span>

## <span data-ttu-id="3b9d7-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b9d7-146">OUTPUTS</span></span>

### <span data-ttu-id="3b9d7-147">Microsoft. Azure. commands. Networks. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="3b9d7-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="3b9d7-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b9d7-148">NOTES</span></span>

## <span data-ttu-id="3b9d7-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b9d7-149">RELATED LINKS</span></span>
