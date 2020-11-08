---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 88AB3621-7C80-41BA-BE49-4F8F9C46BCF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fb0fa13cb5ea155b945505fd3f99c28494c5dc0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099753"
---
# <span data-ttu-id="019ae-101">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="019ae-101">Get-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="019ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="019ae-102">SYNOPSIS</span></span>
<span data-ttu-id="019ae-103">Ansluter till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="019ae-103">Gets a virtual network gateway connection.</span></span>

## <span data-ttu-id="019ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="019ae-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayConnection [-GatewayId <String>] [-ConnectedEntityId <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="019ae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="019ae-105">DESCRIPTION</span></span>
<span data-ttu-id="019ae-106">Cmdleten **Get-AzureVirtualNetworkGatewayConnection** får en Azure Virtual Network Gateway-anslutning.</span><span class="sxs-lookup"><span data-stu-id="019ae-106">The **Get-AzureVirtualNetworkGatewayConnection** cmdlet gets an Azure virtual network gateway connection.</span></span>

## <span data-ttu-id="019ae-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="019ae-107">EXAMPLES</span></span>

## <span data-ttu-id="019ae-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="019ae-108">PARAMETERS</span></span>

### <span data-ttu-id="019ae-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="019ae-109">-ConnectedEntityId</span></span>
<span data-ttu-id="019ae-110">Anger ID för en ansluten enhet.</span><span class="sxs-lookup"><span data-stu-id="019ae-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="019ae-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="019ae-111">-GatewayId</span></span>
<span data-ttu-id="019ae-112">Anger gatewayens ID.</span><span class="sxs-lookup"><span data-stu-id="019ae-112">Specifies the ID of the gateway.</span></span>

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

### <span data-ttu-id="019ae-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="019ae-113">-Profile</span></span>
<span data-ttu-id="019ae-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="019ae-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="019ae-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="019ae-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="019ae-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="019ae-116">CommonParameters</span></span>
<span data-ttu-id="019ae-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="019ae-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="019ae-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="019ae-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="019ae-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="019ae-119">INPUTS</span></span>

## <span data-ttu-id="019ae-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="019ae-120">OUTPUTS</span></span>

## <span data-ttu-id="019ae-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="019ae-121">NOTES</span></span>

## <span data-ttu-id="019ae-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="019ae-122">RELATED LINKS</span></span>

[<span data-ttu-id="019ae-123">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="019ae-123">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="019ae-124">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="019ae-124">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="019ae-125">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="019ae-125">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)
