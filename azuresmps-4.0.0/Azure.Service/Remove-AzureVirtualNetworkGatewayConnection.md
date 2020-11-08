---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F3D44471-50F0-4737-9AF5-3DE7222EAF9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: b9aa386b47c02ed945cad63c00425534d68e66f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093211"
---
# <span data-ttu-id="2ea8d-101">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2ea8d-101">Remove-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="2ea8d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ea8d-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea8d-103">Tar bort en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="2ea8d-103">Removes a virtual network gateway connection.</span></span>

## <span data-ttu-id="2ea8d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ea8d-104">SYNTAX</span></span>

```
Remove-AzureVirtualNetworkGatewayConnection -GatewayId <String> -ConnectedEntityId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2ea8d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ea8d-105">DESCRIPTION</span></span>
<span data-ttu-id="2ea8d-106">Cmdleten **Remove-AzureVirtualNetworkGatewayConnection** tar bort en anslutning till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="2ea8d-106">The **Remove-AzureVirtualNetworkGatewayConnection** cmdlet removes a virtual network gateway connection.</span></span>

## <span data-ttu-id="2ea8d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ea8d-107">EXAMPLES</span></span>

## <span data-ttu-id="2ea8d-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ea8d-108">PARAMETERS</span></span>

### <span data-ttu-id="2ea8d-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="2ea8d-109">-ConnectedEntityId</span></span>
<span data-ttu-id="2ea8d-110">Anger ID för en ansluten enhet.</span><span class="sxs-lookup"><span data-stu-id="2ea8d-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="2ea8d-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="2ea8d-111">-GatewayId</span></span>
<span data-ttu-id="2ea8d-112">Anger ID för en gateway.</span><span class="sxs-lookup"><span data-stu-id="2ea8d-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="2ea8d-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="2ea8d-113">-Profile</span></span>
<span data-ttu-id="2ea8d-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="2ea8d-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2ea8d-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="2ea8d-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2ea8d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea8d-116">CommonParameters</span></span>
<span data-ttu-id="2ea8d-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ea8d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea8d-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ea8d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea8d-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ea8d-119">INPUTS</span></span>

## <span data-ttu-id="2ea8d-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ea8d-120">OUTPUTS</span></span>

## <span data-ttu-id="2ea8d-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ea8d-121">NOTES</span></span>

## <span data-ttu-id="2ea8d-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ea8d-122">RELATED LINKS</span></span>

[<span data-ttu-id="2ea8d-123">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2ea8d-123">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2ea8d-124">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2ea8d-124">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2ea8d-125">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2ea8d-125">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)


