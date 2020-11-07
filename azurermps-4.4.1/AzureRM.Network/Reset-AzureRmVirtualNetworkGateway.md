---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 2b2947ec86e928506624aea49b380db3c4f24bc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757497"
---
# <span data-ttu-id="678bf-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="678bf-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="678bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="678bf-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="678bf-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="678bf-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="678bf-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="678bf-104">DESCRIPTION</span></span>

## <span data-ttu-id="678bf-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="678bf-105">EXAMPLES</span></span>

## <span data-ttu-id="678bf-106">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="678bf-106">PARAMETERS</span></span>

### <span data-ttu-id="678bf-107">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="678bf-107">-GatewayVip</span></span>
<span data-ttu-id="678bf-108">Gatewayens VIP-plats för att återställa viss Gateway-instans (t. ex. om det rör sig om Active-Active aktiva gateways.) Som standard återställer gatewayens primära instans om inget värde skickas.</span><span class="sxs-lookup"><span data-stu-id="678bf-108">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="678bf-109">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="678bf-109">-VirtualNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="678bf-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="678bf-110">-DefaultProfile</span></span>
<span data-ttu-id="678bf-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="678bf-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="678bf-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="678bf-112">CommonParameters</span></span>
<span data-ttu-id="678bf-113">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="678bf-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="678bf-114">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="678bf-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="678bf-115">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="678bf-115">INPUTS</span></span>

### <span data-ttu-id="678bf-116">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="678bf-116">String</span></span>
<span data-ttu-id="678bf-117">Parametern ' GatewayVip ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="678bf-117">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="678bf-118">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="678bf-118">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="678bf-119">Parametern ' VirtualNetworkGateway ' godkänner värdet av typen ' PSVirtualNetworkGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="678bf-119">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="678bf-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="678bf-120">OUTPUTS</span></span>

### <span data-ttu-id="678bf-121">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="678bf-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="678bf-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="678bf-122">NOTES</span></span>

## <span data-ttu-id="678bf-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="678bf-123">RELATED LINKS</span></span>

[<span data-ttu-id="678bf-124">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="678bf-124">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="678bf-125">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="678bf-125">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="678bf-126">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="678bf-126">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="678bf-127">Ändra storlek – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="678bf-127">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="678bf-128">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="678bf-128">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


