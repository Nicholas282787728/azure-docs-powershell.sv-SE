---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5F016D72-80EB-462D-9646-25EC4E33293E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 485b29130fd4b54c378f3ec19389b6c24ba86c63
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099743"
---
# <span data-ttu-id="ab4b0-101">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="ab4b0-101">Get-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="ab4b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab4b0-102">SYNOPSIS</span></span>
<span data-ttu-id="ab4b0-103">Hämtar nyckeln till en Azure Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="ab4b0-103">Gets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="ab4b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab4b0-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab4b0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab4b0-105">DESCRIPTION</span></span>
<span data-ttu-id="ab4b0-106">Cmdleten **Get-AzureVirtualNetworkGatewayKey** hämtar nyckeln till en Azure Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="ab4b0-106">The **Get-AzureVirtualNetworkGatewayKey** cmdlet gets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="ab4b0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab4b0-107">EXAMPLES</span></span>

## <span data-ttu-id="ab4b0-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab4b0-108">PARAMETERS</span></span>

### <span data-ttu-id="ab4b0-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="ab4b0-109">-ConnectedEntityId</span></span>
<span data-ttu-id="ab4b0-110">Anger ID för en ansluten enhet.</span><span class="sxs-lookup"><span data-stu-id="ab4b0-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="ab4b0-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="ab4b0-111">-GatewayId</span></span>
<span data-ttu-id="ab4b0-112">Anger ID för en gateway.</span><span class="sxs-lookup"><span data-stu-id="ab4b0-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="ab4b0-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="ab4b0-113">-Profile</span></span>
<span data-ttu-id="ab4b0-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="ab4b0-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ab4b0-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="ab4b0-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ab4b0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab4b0-116">CommonParameters</span></span>
<span data-ttu-id="ab4b0-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab4b0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab4b0-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab4b0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab4b0-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab4b0-119">INPUTS</span></span>

## <span data-ttu-id="ab4b0-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab4b0-120">OUTPUTS</span></span>

## <span data-ttu-id="ab4b0-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab4b0-121">NOTES</span></span>

## <span data-ttu-id="ab4b0-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab4b0-122">RELATED LINKS</span></span>

[<span data-ttu-id="ab4b0-123">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="ab4b0-123">Reset-AzureVirtualNetworkGatewayKey</span></span>](./Reset-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="ab4b0-124">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="ab4b0-124">Set-AzureVirtualNetworkGatewayKey</span></span>](./Set-AzureVirtualNetworkGatewayKey.md)


