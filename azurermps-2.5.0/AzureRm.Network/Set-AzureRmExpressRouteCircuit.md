---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: a37502abcee157e9666a49ea5db5d2afe206aa8c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930913"
---
# <span data-ttu-id="17b79-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="17b79-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="17b79-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17b79-102">SYNOPSIS</span></span>
<span data-ttu-id="17b79-103">Ändrar en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="17b79-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17b79-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17b79-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17b79-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17b79-105">DESCRIPTION</span></span>
<span data-ttu-id="17b79-106">Cmdleten **set-AzureRmExpressRouteCircuit** sparar den ändrade ExpressRoute-kretsen i Azure.</span><span class="sxs-lookup"><span data-stu-id="17b79-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="17b79-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17b79-107">EXAMPLES</span></span>

### <span data-ttu-id="17b79-108">Exempel 1: ändra ServiceKey för en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="17b79-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="17b79-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17b79-109">PARAMETERS</span></span>

### <span data-ttu-id="17b79-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17b79-110">-AsJob</span></span>
<span data-ttu-id="17b79-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="17b79-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17b79-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17b79-112">-DefaultProfile</span></span>
<span data-ttu-id="17b79-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="17b79-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b79-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="17b79-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="17b79-115">Anger det **ExpressRouteCircuit** -objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="17b79-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17b79-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b79-116">CommonParameters</span></span>
<span data-ttu-id="17b79-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17b79-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b79-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17b79-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b79-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17b79-119">INPUTS</span></span>

### <span data-ttu-id="17b79-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="17b79-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="17b79-121">Parametern ' ExpressRouteCircuit ' godkänner värdet av typen ' PSExpressRouteCircuit ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="17b79-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="17b79-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17b79-122">OUTPUTS</span></span>

### <span data-ttu-id="17b79-123">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="17b79-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="17b79-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17b79-124">NOTES</span></span>

## <span data-ttu-id="17b79-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17b79-125">RELATED LINKS</span></span>

[<span data-ttu-id="17b79-126">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="17b79-126">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="17b79-127">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="17b79-127">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="17b79-128">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="17b79-128">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="17b79-129">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="17b79-129">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)