---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: f4039fb8a616a474a858728b6e222537c2d75c66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931186"
---
# <span data-ttu-id="20d16-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20d16-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="20d16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20d16-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20d16-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20d16-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20d16-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20d16-104">DESCRIPTION</span></span>

## <span data-ttu-id="20d16-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20d16-105">EXAMPLES</span></span>

### <span data-ttu-id="20d16-106">9.1</span><span class="sxs-lookup"><span data-stu-id="20d16-106">1:</span></span>
```

```

## <span data-ttu-id="20d16-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20d16-107">PARAMETERS</span></span>

### <span data-ttu-id="20d16-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20d16-108">-AsJob</span></span>
<span data-ttu-id="20d16-109">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="20d16-109">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20d16-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20d16-110">-DefaultProfile</span></span>
<span data-ttu-id="20d16-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20d16-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20d16-112">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="20d16-112">-GatewayVip</span></span>
<span data-ttu-id="20d16-113">Gatewayens VIP-plats för att återställa viss Gateway-instans (t. ex. om det rör sig om Active-Active aktiva gateways.) Som standard återställer gatewayens primära instans om inget värde skickas.</span><span class="sxs-lookup"><span data-stu-id="20d16-113">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20d16-114">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20d16-114">-VirtualNetworkGateway</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20d16-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20d16-115">CommonParameters</span></span>
<span data-ttu-id="20d16-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20d16-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20d16-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20d16-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20d16-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20d16-118">INPUTS</span></span>

### <span data-ttu-id="20d16-119">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="20d16-119">String</span></span>
<span data-ttu-id="20d16-120">Parametern ' GatewayVip ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="20d16-120">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="20d16-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20d16-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="20d16-122">Parametern ' VirtualNetworkGateway ' godkänner värdet av typen ' PSVirtualNetworkGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="20d16-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="20d16-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20d16-123">OUTPUTS</span></span>

### <span data-ttu-id="20d16-124">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20d16-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="20d16-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20d16-125">NOTES</span></span>

## <span data-ttu-id="20d16-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20d16-126">RELATED LINKS</span></span>

[<span data-ttu-id="20d16-127">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20d16-127">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="20d16-128">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20d16-128">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="20d16-129">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20d16-129">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="20d16-130">Ändra storlek – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20d16-130">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="20d16-131">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20d16-131">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


