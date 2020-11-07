---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 262dd4333b2490c5035a00de179b9b2092ccb71e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924230"
---
# <span data-ttu-id="9de84-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9de84-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="9de84-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9de84-102">SYNOPSIS</span></span>
<span data-ttu-id="9de84-103">Ändrar en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="9de84-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="9de84-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9de84-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9de84-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9de84-105">DESCRIPTION</span></span>
<span data-ttu-id="9de84-106">Cmdleten **set-AzExpressRouteCircuit** sparar den ändrade ExpressRoute-kretsen i Azure.</span><span class="sxs-lookup"><span data-stu-id="9de84-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="9de84-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9de84-107">EXAMPLES</span></span>

### <span data-ttu-id="9de84-108">Exempel 1: ändra ServiceKey för en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="9de84-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="9de84-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9de84-109">PARAMETERS</span></span>

### <span data-ttu-id="9de84-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9de84-110">-AsJob</span></span>
<span data-ttu-id="9de84-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9de84-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9de84-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de84-112">-DefaultProfile</span></span>
<span data-ttu-id="9de84-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9de84-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9de84-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9de84-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="9de84-115">Anger det **ExpressRouteCircuit** -objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="9de84-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9de84-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de84-116">CommonParameters</span></span>
<span data-ttu-id="9de84-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9de84-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de84-118">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9de84-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de84-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9de84-119">INPUTS</span></span>

### <span data-ttu-id="9de84-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9de84-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="9de84-121">Parametern ' ExpressRouteCircuit ' godkänner värdet av typen ' PSExpressRouteCircuit ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9de84-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="9de84-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9de84-122">OUTPUTS</span></span>

### <span data-ttu-id="9de84-123">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9de84-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="9de84-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9de84-124">NOTES</span></span>

## <span data-ttu-id="9de84-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9de84-125">RELATED LINKS</span></span>

[<span data-ttu-id="9de84-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9de84-126">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="9de84-127">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9de84-127">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="9de84-128">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9de84-128">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="9de84-129">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9de84-129">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
