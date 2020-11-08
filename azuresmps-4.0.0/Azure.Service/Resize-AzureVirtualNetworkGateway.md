---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AD5F4D69-45AF-46FB-ADF0-59CEF9908EF7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d63ac418d2dcee97afef9ae5f351fb2c1eebece0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099316"
---
# <span data-ttu-id="79c24-101">Resize-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="79c24-101">Resize-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="79c24-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79c24-102">SYNOPSIS</span></span>
<span data-ttu-id="79c24-103">Ändrar storlek på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="79c24-103">Resizes a virtual network gateway.</span></span>

## <span data-ttu-id="79c24-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79c24-104">SYNTAX</span></span>

```
Resize-AzureVirtualNetworkGateway -GatewayId <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="79c24-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79c24-105">DESCRIPTION</span></span>
<span data-ttu-id="79c24-106">Resize-AzureVirtualNetworkGateway cmdlet ändrar storlek på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="79c24-106">The Resize-AzureVirtualNetworkGateway cmdlet resizes a virtual network gateway.</span></span>

## <span data-ttu-id="79c24-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79c24-107">EXAMPLES</span></span>

## <span data-ttu-id="79c24-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79c24-108">PARAMETERS</span></span>

### <span data-ttu-id="79c24-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="79c24-109">-GatewayId</span></span>
<span data-ttu-id="79c24-110">Anger ID för en gateway.</span><span class="sxs-lookup"><span data-stu-id="79c24-110">Specifies the ID of a gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c24-111">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="79c24-111">-GatewaySKU</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c24-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="79c24-112">-Profile</span></span>
<span data-ttu-id="79c24-113">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="79c24-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="79c24-114">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="79c24-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c24-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c24-115">CommonParameters</span></span>
<span data-ttu-id="79c24-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79c24-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c24-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79c24-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c24-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79c24-118">INPUTS</span></span>

## <span data-ttu-id="79c24-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79c24-119">OUTPUTS</span></span>

## <span data-ttu-id="79c24-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79c24-120">NOTES</span></span>

## <span data-ttu-id="79c24-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79c24-121">RELATED LINKS</span></span>

[<span data-ttu-id="79c24-122">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="79c24-122">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="79c24-123">New-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="79c24-123">New-AzureVirtualNetworkGateway</span></span>](./New-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="79c24-124">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="79c24-124">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="79c24-125">Reset-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="79c24-125">Reset-AzureVirtualNetworkGateway</span></span>](./Reset-AzureVirtualNetworkGateway.md)


