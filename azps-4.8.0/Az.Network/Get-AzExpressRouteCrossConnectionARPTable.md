---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
ms.openlocfilehash: 30addde4594c7b67fd5ba9c1358d64ac206a4531
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258822"
---
# <span data-ttu-id="7d52b-101">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="7d52b-101">Get-AzExpressRouteCrossConnectionArpTable</span></span>

## <span data-ttu-id="7d52b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d52b-102">SYNOPSIS</span></span>
<span data-ttu-id="7d52b-103">Hämtar ARP-tabellen från en ExpressRoute-kors anslutning.</span><span class="sxs-lookup"><span data-stu-id="7d52b-103">Gets the ARP table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="7d52b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d52b-104">SYNTAX</span></span>

### <span data-ttu-id="7d52b-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="7d52b-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d52b-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="7d52b-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d52b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d52b-107">DESCRIPTION</span></span>
<span data-ttu-id="7d52b-108">Cmdleten **Get-AzExpressRouteCrossConnectionARPTable** hämtar ARP-tabellen från båda gränssnitten av en ExpressRoute-kors anslutning.</span><span class="sxs-lookup"><span data-stu-id="7d52b-108">The **Get-AzExpressRouteCrossConnectionARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute cross connection.</span></span> <span data-ttu-id="7d52b-109">ARP-tabellen tillhandahåller en mappning av IPv4-adress till MAC-adress för en viss peering.</span><span class="sxs-lookup"><span data-stu-id="7d52b-109">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="7d52b-110">Du kan använda ARP-tabellen för att verifiera nivå 2-konfiguration och anslutning.</span><span class="sxs-lookup"><span data-stu-id="7d52b-110">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="7d52b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d52b-111">EXAMPLES</span></span>

### <span data-ttu-id="7d52b-112">Exempel 1: Visa ARP-tabellen för en ExpressRoute-peer</span><span class="sxs-lookup"><span data-stu-id="7d52b-112">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCrossConnectionARPTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="7d52b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d52b-113">PARAMETERS</span></span>

### <span data-ttu-id="7d52b-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="7d52b-114">-CrossConnectionName</span></span>
<span data-ttu-id="7d52b-115">Namnet på snabb vägs kors anslutningen</span><span class="sxs-lookup"><span data-stu-id="7d52b-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="7d52b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d52b-116">-DefaultProfile</span></span>
<span data-ttu-id="7d52b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d52b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d52b-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="7d52b-118">-DevicePath</span></span>
<span data-ttu-id="7d52b-119">De acceptabla värdena för denna parameter är: `Primary` eller `Secondary`</span><span class="sxs-lookup"><span data-stu-id="7d52b-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="7d52b-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7d52b-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="7d52b-121">Snabb flödets kors anslutning</span><span class="sxs-lookup"><span data-stu-id="7d52b-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="7d52b-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="7d52b-122">-PeeringType</span></span>
<span data-ttu-id="7d52b-123">De acceptabla värdena för den här parametern är: `AzurePrivatePeering` , `AzurePublicPeering` och `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="7d52b-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="7d52b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d52b-124">-ResourceGroupName</span></span>
<span data-ttu-id="7d52b-125">Namnet på resurs gruppen som innehåller ExpressRoute-kors anslutningen.</span><span class="sxs-lookup"><span data-stu-id="7d52b-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="7d52b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d52b-126">CommonParameters</span></span>
<span data-ttu-id="7d52b-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d52b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d52b-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d52b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d52b-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d52b-129">INPUTS</span></span>

### <span data-ttu-id="7d52b-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="7d52b-130">None</span></span>
<span data-ttu-id="7d52b-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="7d52b-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7d52b-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d52b-132">OUTPUTS</span></span>

### <span data-ttu-id="7d52b-133">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="7d52b-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="7d52b-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d52b-134">NOTES</span></span>

## <span data-ttu-id="7d52b-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d52b-135">RELATED LINKS</span></span>

[<span data-ttu-id="7d52b-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="7d52b-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)

[<span data-ttu-id="7d52b-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7d52b-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
