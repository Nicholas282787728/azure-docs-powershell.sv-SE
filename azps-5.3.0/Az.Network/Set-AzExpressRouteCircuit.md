---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 58df8e57a225d1ee003da317ca24c71b1db34f5f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525797"
---
# <span data-ttu-id="f97db-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f97db-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="f97db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f97db-102">SYNOPSIS</span></span>
<span data-ttu-id="f97db-103">Ändrar en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="f97db-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="f97db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f97db-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f97db-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f97db-105">DESCRIPTION</span></span>
<span data-ttu-id="f97db-106">Cmdleten **set-AzExpressRouteCircuit** sparar den ändrade ExpressRoute-kretsen i Azure.</span><span class="sxs-lookup"><span data-stu-id="f97db-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="f97db-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f97db-107">EXAMPLES</span></span>

### <span data-ttu-id="f97db-108">Exempel 1: ändra ServiceKey för en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="f97db-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="f97db-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f97db-109">PARAMETERS</span></span>

### <span data-ttu-id="f97db-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f97db-110">-AsJob</span></span>
<span data-ttu-id="f97db-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f97db-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f97db-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f97db-112">-DefaultProfile</span></span>
<span data-ttu-id="f97db-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f97db-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f97db-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f97db-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="f97db-115">Anger det **ExpressRouteCircuit** -objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="f97db-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f97db-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f97db-116">CommonParameters</span></span>
<span data-ttu-id="f97db-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f97db-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f97db-118">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f97db-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f97db-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f97db-119">INPUTS</span></span>

### <span data-ttu-id="f97db-120">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f97db-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f97db-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f97db-121">OUTPUTS</span></span>

### <span data-ttu-id="f97db-122">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f97db-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f97db-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f97db-123">NOTES</span></span>

## <span data-ttu-id="f97db-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f97db-124">RELATED LINKS</span></span>

[<span data-ttu-id="f97db-125">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f97db-125">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="f97db-126">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f97db-126">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="f97db-127">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f97db-127">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="f97db-128">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f97db-128">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
