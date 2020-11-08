---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F6A89D39-18AD-4087-823C-63FA0A3690E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36c51d0ceae42aab50e2df9e0532c98dd6800747
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099750"
---
# <span data-ttu-id="d73b5-101">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d73b5-101">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="d73b5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d73b5-102">SYNOPSIS</span></span>
<span data-ttu-id="d73b5-103">Hämtar resultaten från Azure Virtual Network Gateway Diagnostics.</span><span class="sxs-lookup"><span data-stu-id="d73b5-103">Gets the results of Azure virtual network gateway diagnostics.</span></span>

## <span data-ttu-id="d73b5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d73b5-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d73b5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d73b5-105">DESCRIPTION</span></span>
<span data-ttu-id="d73b5-106">Cmdleten **Get-AzureVirtualNetworkGatewayDiagnostics** hämtar resultaten från diagnostik för Azure Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="d73b5-106">The **Get-AzureVirtualNetworkGatewayDiagnostics** cmdlet gets the results of Azure virtual network gateway diagnostics.</span></span>

## <span data-ttu-id="d73b5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d73b5-107">EXAMPLES</span></span>

## <span data-ttu-id="d73b5-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d73b5-108">PARAMETERS</span></span>

### <span data-ttu-id="d73b5-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="d73b5-109">-GatewayId</span></span>
<span data-ttu-id="d73b5-110">Anger ID för en gateway.</span><span class="sxs-lookup"><span data-stu-id="d73b5-110">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="d73b5-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="d73b5-111">-Profile</span></span>
<span data-ttu-id="d73b5-112">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="d73b5-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d73b5-113">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="d73b5-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d73b5-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d73b5-114">CommonParameters</span></span>
<span data-ttu-id="d73b5-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d73b5-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d73b5-116">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d73b5-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d73b5-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d73b5-117">INPUTS</span></span>

## <span data-ttu-id="d73b5-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d73b5-118">OUTPUTS</span></span>

## <span data-ttu-id="d73b5-119">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d73b5-119">NOTES</span></span>

## <span data-ttu-id="d73b5-120">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d73b5-120">RELATED LINKS</span></span>

[<span data-ttu-id="d73b5-121">Start-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d73b5-121">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Start-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="d73b5-122">Stopp-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d73b5-122">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Stop-AzureVirtualNetworkGatewayDiagnostics.md)


