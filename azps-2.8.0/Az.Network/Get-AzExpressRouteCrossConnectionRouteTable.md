---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
ms.openlocfilehash: 3fbfcc2ba78bb05eb64764be16bb84189afdd958
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918499"
---
# <span data-ttu-id="a11cd-101">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a11cd-101">Get-AzExpressRouteCrossConnectionRouteTable</span></span>

## <span data-ttu-id="a11cd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a11cd-102">SYNOPSIS</span></span>
<span data-ttu-id="a11cd-103">Hämtar en routningstabell från en ExpressRoute kors koppling.</span><span class="sxs-lookup"><span data-stu-id="a11cd-103">Gets a route table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="a11cd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a11cd-104">SYNTAX</span></span>

### <span data-ttu-id="a11cd-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="a11cd-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a11cd-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="a11cd-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a11cd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a11cd-107">DESCRIPTION</span></span>
<span data-ttu-id="a11cd-108">Cmdleten **Get-AzExpressRouteCrossConnectionRouteTable** hämtar en detaljerad vägkälla för en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="a11cd-108">The **Get-AzExpressRouteCrossConnectionRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="a11cd-109">Routningstabellen visar alla vägar eller kan filtreras för att Visa vägar för en viss peering-typ.</span><span class="sxs-lookup"><span data-stu-id="a11cd-109">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="a11cd-110">Du kan använda routningstabellen för att validera din konfiguration och anslutnings barhet för din peering.</span><span class="sxs-lookup"><span data-stu-id="a11cd-110">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="a11cd-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a11cd-111">EXAMPLES</span></span>

### <span data-ttu-id="a11cd-112">Exempel 1: Visa routningstabellen för den primära sökvägen</span><span class="sxs-lookup"><span data-stu-id="a11cd-112">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="a11cd-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a11cd-113">PARAMETERS</span></span>

### <span data-ttu-id="a11cd-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="a11cd-114">-CrossConnectionName</span></span>
<span data-ttu-id="a11cd-115">Namnet på snabb vägs kors anslutningen</span><span class="sxs-lookup"><span data-stu-id="a11cd-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="a11cd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a11cd-116">-DefaultProfile</span></span>
<span data-ttu-id="a11cd-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a11cd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a11cd-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="a11cd-118">-DevicePath</span></span>
<span data-ttu-id="a11cd-119">De acceptabla värdena för denna parameter är: `Primary` eller `Secondary`</span><span class="sxs-lookup"><span data-stu-id="a11cd-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="a11cd-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a11cd-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="a11cd-121">Snabb flödets kors anslutning</span><span class="sxs-lookup"><span data-stu-id="a11cd-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="a11cd-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="a11cd-122">-PeeringType</span></span>
<span data-ttu-id="a11cd-123">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="a11cd-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="a11cd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a11cd-124">-ResourceGroupName</span></span>
<span data-ttu-id="a11cd-125">Namnet på resurs gruppen som innehåller ExpressRoute-kors anslutningen.</span><span class="sxs-lookup"><span data-stu-id="a11cd-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="a11cd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a11cd-126">CommonParameters</span></span>
<span data-ttu-id="a11cd-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a11cd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a11cd-128">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a11cd-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a11cd-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a11cd-129">INPUTS</span></span>

### <span data-ttu-id="a11cd-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="a11cd-130">None</span></span>
<span data-ttu-id="a11cd-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a11cd-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a11cd-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a11cd-132">OUTPUTS</span></span>

### <span data-ttu-id="a11cd-133">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="a11cd-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="a11cd-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a11cd-134">NOTES</span></span>

## <span data-ttu-id="a11cd-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a11cd-135">RELATED LINKS</span></span>

[<span data-ttu-id="a11cd-136">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="a11cd-136">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="a11cd-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a11cd-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
