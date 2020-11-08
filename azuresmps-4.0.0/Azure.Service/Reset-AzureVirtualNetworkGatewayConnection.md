---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 09642B94-E888-4A22-9E8E-62109DB9394E
online version: ''
schema: 2.0.0
ms.openlocfilehash: f42a788f29f8546e6f402f1685f4c91aa3d7e5cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099319"
---
# <span data-ttu-id="6e055-101">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6e055-101">Reset-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="6e055-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e055-102">SYNOPSIS</span></span>
<span data-ttu-id="6e055-103">Återställer en anslutning till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="6e055-103">Resets a virtual network gateway connection.</span></span>

## <span data-ttu-id="6e055-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e055-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGatewayConnection -GatewayId <String> -ConnectedEntityId <String>
 -RoutingWeight <Int32> [-SharedKey <String>] [-EnableBgp <Boolean>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e055-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e055-105">DESCRIPTION</span></span>
<span data-ttu-id="6e055-106">Cmdleten **Reset-AzureVirtualNetworkGatewayConnection** återställer en anslutning till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="6e055-106">The **Reset-AzureVirtualNetworkGatewayConnection** cmdlet resets a virtual network gateway connection.</span></span>

## <span data-ttu-id="6e055-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e055-107">EXAMPLES</span></span>

## <span data-ttu-id="6e055-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e055-108">PARAMETERS</span></span>

### <span data-ttu-id="6e055-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="6e055-109">-ConnectedEntityId</span></span>
<span data-ttu-id="6e055-110">Anger ID för en ansluten enhet.</span><span class="sxs-lookup"><span data-stu-id="6e055-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="6e055-111">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="6e055-111">-EnableBgp</span></span>
<span data-ttu-id="6e055-112">Aktiverar BGP (Border Gateway Protocol).</span><span class="sxs-lookup"><span data-stu-id="6e055-112">Enables Border Gateway Protocol (BGP).</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e055-113">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="6e055-113">-GatewayId</span></span>
<span data-ttu-id="6e055-114">Anger ID för en gateway.</span><span class="sxs-lookup"><span data-stu-id="6e055-114">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="6e055-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="6e055-115">-Profile</span></span>
<span data-ttu-id="6e055-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="6e055-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="6e055-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="6e055-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6e055-118">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="6e055-118">-RoutingWeight</span></span>
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

### <span data-ttu-id="6e055-119">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="6e055-119">-SharedKey</span></span>
<span data-ttu-id="6e055-120">Anger en delad nycklar.</span><span class="sxs-lookup"><span data-stu-id="6e055-120">Specifies a shared key.</span></span>

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

### <span data-ttu-id="6e055-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e055-121">CommonParameters</span></span>
<span data-ttu-id="6e055-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e055-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e055-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e055-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e055-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e055-124">INPUTS</span></span>

## <span data-ttu-id="6e055-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e055-125">OUTPUTS</span></span>

## <span data-ttu-id="6e055-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e055-126">NOTES</span></span>

## <span data-ttu-id="6e055-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e055-127">RELATED LINKS</span></span>

[<span data-ttu-id="6e055-128">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6e055-128">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="6e055-129">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6e055-129">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="6e055-130">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6e055-130">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)


