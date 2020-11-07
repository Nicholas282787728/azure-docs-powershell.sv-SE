---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: b223cf62b536479b4c39d5852974698f2f38becf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757490"
---
# <span data-ttu-id="f4b7c-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f4b7c-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="f4b7c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b7c-103">Ändrar en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="f4b7c-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4b7c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4b7c-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4b7c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4b7c-105">DESCRIPTION</span></span>
<span data-ttu-id="f4b7c-106">Cmdleten **set-AzureRmExpressRouteCircuit** sparar den ändrade ExpressRoute-kretsen i Azure.</span><span class="sxs-lookup"><span data-stu-id="f4b7c-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="f4b7c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4b7c-107">EXAMPLES</span></span>

### <span data-ttu-id="f4b7c-108">Exempel 1: ändra ServiceKey för en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="f4b7c-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="f4b7c-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4b7c-109">PARAMETERS</span></span>

### <span data-ttu-id="f4b7c-110">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f4b7c-110">-ExpressRouteCircuit</span></span>
<span data-ttu-id="f4b7c-111">Anger det **ExpressRouteCircuit** -objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="f4b7c-111">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f4b7c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4b7c-112">-DefaultProfile</span></span>
<span data-ttu-id="f4b7c-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f4b7c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4b7c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b7c-114">CommonParameters</span></span>
<span data-ttu-id="f4b7c-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4b7c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b7c-116">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4b7c-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b7c-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4b7c-117">INPUTS</span></span>

### <span data-ttu-id="f4b7c-118">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f4b7c-118">PSExpressRouteCircuit</span></span>
<span data-ttu-id="f4b7c-119">Parametern ' ExpressRouteCircuit ' godkänner värdet av typen ' PSExpressRouteCircuit ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f4b7c-119">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="f4b7c-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4b7c-120">OUTPUTS</span></span>

### <span data-ttu-id="f4b7c-121">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f4b7c-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f4b7c-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4b7c-122">NOTES</span></span>

## <span data-ttu-id="f4b7c-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4b7c-123">RELATED LINKS</span></span>

[<span data-ttu-id="f4b7c-124">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f4b7c-124">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="f4b7c-125">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f4b7c-125">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="f4b7c-126">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f4b7c-126">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="f4b7c-127">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f4b7c-127">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)
