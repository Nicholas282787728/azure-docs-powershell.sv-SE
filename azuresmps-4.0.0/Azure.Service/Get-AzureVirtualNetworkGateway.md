---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C4F876DF-FA9A-4446-8B7B-735137CEFE5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: eccd46bac70cb6555277b66f45cf2e79ad10e1e7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099755"
---
# <span data-ttu-id="b1f42-101">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1f42-101">Get-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="b1f42-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b1f42-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f42-103">Hämtar en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="b1f42-103">Gets a virtual network gateway.</span></span>

## <span data-ttu-id="b1f42-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b1f42-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGateway [-GatewayId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b1f42-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b1f42-105">DESCRIPTION</span></span>
<span data-ttu-id="b1f42-106">Cmdleten **Get-AzureVirtualNetworkGateway** får en Azure Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="b1f42-106">The **Get-AzureVirtualNetworkGateway** cmdlet gets an Azure virtual network gateway.</span></span>

## <span data-ttu-id="b1f42-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b1f42-107">EXAMPLES</span></span>

## <span data-ttu-id="b1f42-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b1f42-108">PARAMETERS</span></span>

### <span data-ttu-id="b1f42-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="b1f42-109">-GatewayId</span></span>
<span data-ttu-id="b1f42-110">Anger gatewayens ID.</span><span class="sxs-lookup"><span data-stu-id="b1f42-110">Specifies the ID of the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1f42-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="b1f42-111">-Profile</span></span>
<span data-ttu-id="b1f42-112">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="b1f42-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b1f42-113">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="b1f42-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b1f42-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f42-114">CommonParameters</span></span>
<span data-ttu-id="b1f42-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1f42-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f42-116">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1f42-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f42-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b1f42-117">INPUTS</span></span>

## <span data-ttu-id="b1f42-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b1f42-118">OUTPUTS</span></span>

## <span data-ttu-id="b1f42-119">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b1f42-119">NOTES</span></span>

## <span data-ttu-id="b1f42-120">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b1f42-120">RELATED LINKS</span></span>

[<span data-ttu-id="b1f42-121">New-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1f42-121">New-AzureVirtualNetworkGateway</span></span>](./New-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="b1f42-122">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1f42-122">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="b1f42-123">Reset-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1f42-123">Reset-AzureVirtualNetworkGateway</span></span>](./Reset-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="b1f42-124">Ändra storlek – AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1f42-124">Resize-AzureVirtualNetworkGateway</span></span>](./Resize-AzureVirtualNetworkGateway.md)


