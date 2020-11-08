---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: E3C0C3AA-3941-469E-A6CC-A92ADD7377B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bf6824219879af52549d7815d65dcb502a2a752
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099415"
---
# <span data-ttu-id="96064-101">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="96064-101">New-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="96064-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96064-102">SYNOPSIS</span></span>
<span data-ttu-id="96064-103">Skapar en Azure Virtual Gateway-nätverks anslutning.</span><span class="sxs-lookup"><span data-stu-id="96064-103">Creates an Azure virtual gateway network connection.</span></span>

## <span data-ttu-id="96064-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96064-104">SYNTAX</span></span>

```
New-AzureVirtualNetworkGatewayConnection -ConnectedEntityId <String> -GatewayConnectionName <String>
 -GatewayConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>]
 -VirtualNetworkGatewayId <String> [-EnableBgp <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="96064-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96064-105">DESCRIPTION</span></span>
<span data-ttu-id="96064-106">Cmdleten **New-AzureVirtualNetworkGatewayConnection** skapar en Azure Virtual Gateway-nätverksanslutning.</span><span class="sxs-lookup"><span data-stu-id="96064-106">The **New-AzureVirtualNetworkGatewayConnection** cmdlet creates an Azure virtual gateway network connection.</span></span>

## <span data-ttu-id="96064-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96064-107">EXAMPLES</span></span>

## <span data-ttu-id="96064-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96064-108">PARAMETERS</span></span>

### <span data-ttu-id="96064-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="96064-109">-ConnectedEntityId</span></span>
<span data-ttu-id="96064-110">Anger ID för en ansluten enhet.</span><span class="sxs-lookup"><span data-stu-id="96064-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="96064-111">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="96064-111">-EnableBgp</span></span>
<span data-ttu-id="96064-112">Aktiverar BGP (Border Gateway Protocol).</span><span class="sxs-lookup"><span data-stu-id="96064-112">Enables Border Gateway Protocol (BGP).</span></span>

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

### <span data-ttu-id="96064-113">-GatewayConnectionName</span><span class="sxs-lookup"><span data-stu-id="96064-113">-GatewayConnectionName</span></span>
<span data-ttu-id="96064-114">Anger ett namn för gateway-anslutningen.</span><span class="sxs-lookup"><span data-stu-id="96064-114">Specifies a name for the gateway connection.</span></span>

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

### <span data-ttu-id="96064-115">-GatewayConnectionType</span><span class="sxs-lookup"><span data-stu-id="96064-115">-GatewayConnectionType</span></span>
<span data-ttu-id="96064-116">Anger typen av Gateway-anslutning.</span><span class="sxs-lookup"><span data-stu-id="96064-116">Specifies the type of gateway connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96064-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="96064-117">-Profile</span></span>
<span data-ttu-id="96064-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="96064-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="96064-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="96064-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="96064-120">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="96064-120">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96064-121">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="96064-121">-SharedKey</span></span>
<span data-ttu-id="96064-122">Anger en delad nycklar.</span><span class="sxs-lookup"><span data-stu-id="96064-122">Specifies a shared key.</span></span>

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

### <span data-ttu-id="96064-123">-VirtualNetworkGatewayId</span><span class="sxs-lookup"><span data-stu-id="96064-123">-VirtualNetworkGatewayId</span></span>
<span data-ttu-id="96064-124">Anger ID för en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="96064-124">Specifies the ID of a virtual network gateway.</span></span>

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

### <span data-ttu-id="96064-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96064-125">CommonParameters</span></span>
<span data-ttu-id="96064-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96064-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96064-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96064-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96064-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96064-128">INPUTS</span></span>

## <span data-ttu-id="96064-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96064-129">OUTPUTS</span></span>

## <span data-ttu-id="96064-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96064-130">NOTES</span></span>

## <span data-ttu-id="96064-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96064-131">RELATED LINKS</span></span>

[<span data-ttu-id="96064-132">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="96064-132">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="96064-133">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="96064-133">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="96064-134">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="96064-134">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)


