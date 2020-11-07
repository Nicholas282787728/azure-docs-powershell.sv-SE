---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
ms.openlocfilehash: 5e0d9140e11ead75a1abbf43d520d44cffaf5463
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748307"
---
# <span data-ttu-id="b69f0-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b69f0-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

## <span data-ttu-id="b69f0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b69f0-102">SYNOPSIS</span></span>
<span data-ttu-id="b69f0-103">Hämtar en väg tabell Sammanfattning av en ExpressRoute kors koppling.</span><span class="sxs-lookup"><span data-stu-id="b69f0-103">Gets a route table summary of an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="b69f0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b69f0-104">SYNTAX</span></span>

### <span data-ttu-id="b69f0-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="b69f0-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b69f0-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="b69f0-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b69f0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b69f0-107">DESCRIPTION</span></span>
<span data-ttu-id="b69f0-108">Cmdleten **Get-AzExpressRouteCrossConnectionRouteTableSummary** returnerar en sammanfattning av BGP Neighbor-informationen för en viss kontext för routning.</span><span class="sxs-lookup"><span data-stu-id="b69f0-108">The **Get-AzExpressRouteCrossConnectionRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="b69f0-109">Den här informationen är användbar för att avgöra hur länge en routningsdomän har upprättats och antalet väg-prefix som annonseras av peering router.</span><span class="sxs-lookup"><span data-stu-id="b69f0-109">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="b69f0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b69f0-110">EXAMPLES</span></span>

### <span data-ttu-id="b69f0-111">Exempel 1: Visa väg översikten för den primära sökvägen</span><span class="sxs-lookup"><span data-stu-id="b69f0-111">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -DevicePath 'Primary'
```

## <span data-ttu-id="b69f0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b69f0-112">PARAMETERS</span></span>

### <span data-ttu-id="b69f0-113">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="b69f0-113">-CrossConnectionName</span></span>
<span data-ttu-id="b69f0-114">Namnet på snabb vägs kors anslutningen</span><span class="sxs-lookup"><span data-stu-id="b69f0-114">The Name of Express Route Cross Connection</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b69f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b69f0-115">-DefaultProfile</span></span>
<span data-ttu-id="b69f0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b69f0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b69f0-117">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="b69f0-117">-DevicePath</span></span>
<span data-ttu-id="b69f0-118">De acceptabla värdena för denna parameter är: `Primary` eller `Secondary`</span><span class="sxs-lookup"><span data-stu-id="b69f0-118">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b69f0-119">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b69f0-119">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="b69f0-120">Snabb flödets kors anslutning</span><span class="sxs-lookup"><span data-stu-id="b69f0-120">The Express Route Cross Connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: SpecifyByReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b69f0-121">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="b69f0-121">-PeeringType</span></span>
<span data-ttu-id="b69f0-122">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="b69f0-122">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b69f0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b69f0-123">-ResourceGroupName</span></span>
<span data-ttu-id="b69f0-124">Namnet på resurs gruppen som innehåller ExpressRoute-kors anslutningen.</span><span class="sxs-lookup"><span data-stu-id="b69f0-124">The name of the resource group containing the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b69f0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b69f0-125">CommonParameters</span></span>
<span data-ttu-id="b69f0-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b69f0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b69f0-127">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b69f0-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b69f0-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b69f0-128">INPUTS</span></span>

### <span data-ttu-id="b69f0-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="b69f0-129">None</span></span>
<span data-ttu-id="b69f0-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b69f0-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b69f0-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b69f0-131">OUTPUTS</span></span>

### <span data-ttu-id="b69f0-132">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCrossConnectionRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="b69f0-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span></span>

## <span data-ttu-id="b69f0-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b69f0-133">NOTES</span></span>

## <span data-ttu-id="b69f0-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b69f0-134">RELATED LINKS</span></span>

[<span data-ttu-id="b69f0-135">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="b69f0-135">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="b69f0-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="b69f0-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)
