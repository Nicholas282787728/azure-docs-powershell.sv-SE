---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8099942A-B6EB-4C01-9F57-378B0EB7B3C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c933b716095392a215543cfc61d334cd347835
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093163"
---
# <span data-ttu-id="3f434-101">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="3f434-101">Set-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="3f434-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f434-102">SYNOPSIS</span></span>
<span data-ttu-id="3f434-103">Ställer in nyckeln för en Azure Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="3f434-103">Sets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="3f434-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f434-104">SYNTAX</span></span>

```
Set-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3f434-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f434-105">DESCRIPTION</span></span>
<span data-ttu-id="3f434-106">Cmdleten **set-AzureVirtualNetworkGatewayKey** anger nyckeln för en Azure Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="3f434-106">The **Set-AzureVirtualNetworkGatewayKey** cmdlet sets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="3f434-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f434-107">EXAMPLES</span></span>

## <span data-ttu-id="3f434-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f434-108">PARAMETERS</span></span>

### <span data-ttu-id="3f434-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="3f434-109">-ConnectedEntityId</span></span>
<span data-ttu-id="3f434-110">Anger ID för en ansluten enhet.</span><span class="sxs-lookup"><span data-stu-id="3f434-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="3f434-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="3f434-111">-GatewayId</span></span>
<span data-ttu-id="3f434-112">Anger ID för en gateway.</span><span class="sxs-lookup"><span data-stu-id="3f434-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="3f434-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="3f434-113">-Profile</span></span>
<span data-ttu-id="3f434-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="3f434-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3f434-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="3f434-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3f434-116">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="3f434-116">-SharedKey</span></span>
<span data-ttu-id="3f434-117">Anger en delad nycklar.</span><span class="sxs-lookup"><span data-stu-id="3f434-117">Specifies a shared key.</span></span>

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

### <span data-ttu-id="3f434-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f434-118">CommonParameters</span></span>
<span data-ttu-id="3f434-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f434-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f434-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f434-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f434-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f434-121">INPUTS</span></span>

## <span data-ttu-id="3f434-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f434-122">OUTPUTS</span></span>

## <span data-ttu-id="3f434-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f434-123">NOTES</span></span>

## <span data-ttu-id="3f434-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f434-124">RELATED LINKS</span></span>

[<span data-ttu-id="3f434-125">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="3f434-125">Get-AzureVirtualNetworkGatewayKey</span></span>](./Get-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="3f434-126">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="3f434-126">Reset-AzureVirtualNetworkGatewayKey</span></span>](./Reset-AzureVirtualNetworkGatewayKey.md)


