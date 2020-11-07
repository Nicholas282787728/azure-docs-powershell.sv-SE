---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 815f7d3fdc0f058f2abfce5687b129054814adab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757654"
---
# <span data-ttu-id="7ff79-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7ff79-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="7ff79-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ff79-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ff79-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ff79-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ff79-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ff79-104">DESCRIPTION</span></span>

## <span data-ttu-id="7ff79-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ff79-105">EXAMPLES</span></span>

## <span data-ttu-id="7ff79-106">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ff79-106">PARAMETERS</span></span>

### <span data-ttu-id="7ff79-107">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ff79-107">-AsJob</span></span>
<span data-ttu-id="7ff79-108">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7ff79-108">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ff79-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ff79-109">-DefaultProfile</span></span>
<span data-ttu-id="7ff79-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7ff79-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ff79-111">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="7ff79-111">-GatewayVip</span></span>
<span data-ttu-id="7ff79-112">Gatewayens VIP-plats för att återställa viss Gateway-instans (t. ex. om det rör sig om Active-Active aktiva gateways.) Som standard återställer gatewayens primära instans om inget värde skickas.</span><span class="sxs-lookup"><span data-stu-id="7ff79-112">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="7ff79-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7ff79-113">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="7ff79-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ff79-114">CommonParameters</span></span>
<span data-ttu-id="7ff79-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ff79-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ff79-116">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ff79-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ff79-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ff79-117">INPUTS</span></span>

### <span data-ttu-id="7ff79-118">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="7ff79-118">String</span></span>
<span data-ttu-id="7ff79-119">Parametern ' GatewayVip ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="7ff79-119">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="7ff79-120">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7ff79-120">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="7ff79-121">Parametern ' VirtualNetworkGateway ' godkänner värdet av typen ' PSVirtualNetworkGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="7ff79-121">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="7ff79-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ff79-122">OUTPUTS</span></span>

### <span data-ttu-id="7ff79-123">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7ff79-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7ff79-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ff79-124">NOTES</span></span>

## <span data-ttu-id="7ff79-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ff79-125">RELATED LINKS</span></span>

[<span data-ttu-id="7ff79-126">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7ff79-126">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="7ff79-127">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7ff79-127">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="7ff79-128">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7ff79-128">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="7ff79-129">Ändra storlek – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7ff79-129">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="7ff79-130">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7ff79-130">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


