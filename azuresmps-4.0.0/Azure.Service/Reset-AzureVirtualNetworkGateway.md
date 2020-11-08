---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: CD735391-62A8-40EC-B2F1-9044DC0676CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1cc46fb250a7bc76d05193ea231c81d61668e853
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099320"
---
# <span data-ttu-id="19eda-101">Reset-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="19eda-101">Reset-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="19eda-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19eda-102">SYNOPSIS</span></span>
<span data-ttu-id="19eda-103">Återställer en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="19eda-103">Resets a virtual network gateway.</span></span>

## <span data-ttu-id="19eda-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19eda-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGateway -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="19eda-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19eda-105">DESCRIPTION</span></span>
<span data-ttu-id="19eda-106">Cmdleten **Reset-AzureVirtualNetworkGateway** återställer en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="19eda-106">The **Reset-AzureVirtualNetworkGateway** cmdlet resets a virtual network gateway.</span></span>

## <span data-ttu-id="19eda-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19eda-107">EXAMPLES</span></span>

## <span data-ttu-id="19eda-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19eda-108">PARAMETERS</span></span>

### <span data-ttu-id="19eda-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="19eda-109">-GatewayId</span></span>
<span data-ttu-id="19eda-110">Anger ID för en gateway.</span><span class="sxs-lookup"><span data-stu-id="19eda-110">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="19eda-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="19eda-111">-Profile</span></span>
<span data-ttu-id="19eda-112">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="19eda-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="19eda-113">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="19eda-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="19eda-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19eda-114">CommonParameters</span></span>
<span data-ttu-id="19eda-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19eda-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19eda-116">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19eda-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19eda-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19eda-117">INPUTS</span></span>

## <span data-ttu-id="19eda-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19eda-118">OUTPUTS</span></span>

## <span data-ttu-id="19eda-119">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19eda-119">NOTES</span></span>

## <span data-ttu-id="19eda-120">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19eda-120">RELATED LINKS</span></span>

[<span data-ttu-id="19eda-121">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="19eda-121">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="19eda-122">New-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="19eda-122">New-AzureVirtualNetworkGateway</span></span>](./New-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="19eda-123">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="19eda-123">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="19eda-124">Ändra storlek – AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="19eda-124">Resize-AzureVirtualNetworkGateway</span></span>](./Resize-AzureVirtualNetworkGateway.md)


