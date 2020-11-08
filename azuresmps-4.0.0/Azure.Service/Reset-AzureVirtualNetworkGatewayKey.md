---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4F1E69B8-15FB-495F-B910-04E450D3215F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a5b53f909b840a761d40f79a311fb61b7e2337b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099318"
---
# <span data-ttu-id="76129-101">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="76129-101">Reset-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="76129-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76129-102">SYNOPSIS</span></span>
<span data-ttu-id="76129-103">Återställer en virtuell nätverksgateway-nyckeln.</span><span class="sxs-lookup"><span data-stu-id="76129-103">Resets a virtual network gateway key.</span></span>

## <span data-ttu-id="76129-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76129-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> -keyLength <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="76129-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76129-105">DESCRIPTION</span></span>
<span data-ttu-id="76129-106">Cmdleten **Reset-AzureVirtualNetworkGatewayKey** återställer en virtuell nätverksgateway för gateway.</span><span class="sxs-lookup"><span data-stu-id="76129-106">The **Reset-AzureVirtualNetworkGatewayKey** cmdlet resets a virtual network gateway key.</span></span>

## <span data-ttu-id="76129-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76129-107">EXAMPLES</span></span>

## <span data-ttu-id="76129-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76129-108">PARAMETERS</span></span>

### <span data-ttu-id="76129-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="76129-109">-ConnectedEntityId</span></span>
<span data-ttu-id="76129-110">Anger ID för en ansluten enhet.</span><span class="sxs-lookup"><span data-stu-id="76129-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="76129-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="76129-111">-GatewayId</span></span>
<span data-ttu-id="76129-112">Anger ID för en gateway.</span><span class="sxs-lookup"><span data-stu-id="76129-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="76129-113">-Nyckel längd</span><span class="sxs-lookup"><span data-stu-id="76129-113">-keyLength</span></span>
<span data-ttu-id="76129-114">Anger nyckel längden.</span><span class="sxs-lookup"><span data-stu-id="76129-114">Specifies the key length.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76129-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="76129-115">-Profile</span></span>
<span data-ttu-id="76129-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="76129-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="76129-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="76129-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="76129-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76129-118">CommonParameters</span></span>
<span data-ttu-id="76129-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76129-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76129-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76129-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76129-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76129-121">INPUTS</span></span>

## <span data-ttu-id="76129-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76129-122">OUTPUTS</span></span>

## <span data-ttu-id="76129-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76129-123">NOTES</span></span>

## <span data-ttu-id="76129-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76129-124">RELATED LINKS</span></span>

[<span data-ttu-id="76129-125">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="76129-125">Get-AzureVirtualNetworkGatewayKey</span></span>](./Get-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="76129-126">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="76129-126">Set-AzureVirtualNetworkGatewayKey</span></span>](./Set-AzureVirtualNetworkGatewayKey.md)
