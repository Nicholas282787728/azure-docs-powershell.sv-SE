---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 425008DB-9761-42F1-8D6D-F35757A3CA6C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37aa0718c4faa637b16ccde61f5e5b241bb9aa92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099745"
---
# <span data-ttu-id="02027-101">Get-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="02027-101">Get-AzureVirtualNetworkGatewayIPsecParameters</span></span>

## <span data-ttu-id="02027-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02027-102">SYNOPSIS</span></span>
<span data-ttu-id="02027-103">Hämtar IPsec-parametrar för en Azure Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="02027-103">Gets the IPsec parameters for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="02027-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02027-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayIPsecParameters -GatewayId <String> -ConnectedEntityId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="02027-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02027-105">DESCRIPTION</span></span>
<span data-ttu-id="02027-106">Cmdleten **Get-AzureVirtualNetworkGatewayIPsecParameters** hämtar IPSec-parametrarna för en Azure Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="02027-106">The **Get-AzureVirtualNetworkGatewayIPsecParameters** cmdlet gets the IPsec parameters for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="02027-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02027-107">EXAMPLES</span></span>

## <span data-ttu-id="02027-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02027-108">PARAMETERS</span></span>

### <span data-ttu-id="02027-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="02027-109">-ConnectedEntityId</span></span>
<span data-ttu-id="02027-110">Anger ID för en ansluten entitiy.</span><span class="sxs-lookup"><span data-stu-id="02027-110">Specifies the ID of a connected entitiy.</span></span>

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

### <span data-ttu-id="02027-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="02027-111">-GatewayId</span></span>
<span data-ttu-id="02027-112">Anger ID för en gateway.</span><span class="sxs-lookup"><span data-stu-id="02027-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="02027-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="02027-113">-Profile</span></span>
<span data-ttu-id="02027-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="02027-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="02027-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="02027-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="02027-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02027-116">CommonParameters</span></span>
<span data-ttu-id="02027-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02027-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02027-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02027-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02027-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02027-119">INPUTS</span></span>

## <span data-ttu-id="02027-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02027-120">OUTPUTS</span></span>

## <span data-ttu-id="02027-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02027-121">NOTES</span></span>

## <span data-ttu-id="02027-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02027-122">RELATED LINKS</span></span>

[<span data-ttu-id="02027-123">Set-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="02027-123">Set-AzureVirtualNetworkGatewayIPsecParameters</span></span>](./Set-AzureVirtualNetworkGatewayIPsecParameters.md)


