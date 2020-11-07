---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 53a4eb40d82a721c93102067c8c7e9fe0cbd86be
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924309"
---
# <span data-ttu-id="60b61-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="60b61-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="60b61-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60b61-102">SYNOPSIS</span></span>

## <span data-ttu-id="60b61-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60b61-103">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60b61-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60b61-104">DESCRIPTION</span></span>

## <span data-ttu-id="60b61-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60b61-105">EXAMPLES</span></span>

### <span data-ttu-id="60b61-106">9.1</span><span class="sxs-lookup"><span data-stu-id="60b61-106">1:</span></span>
```

```

## <span data-ttu-id="60b61-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60b61-107">PARAMETERS</span></span>

### <span data-ttu-id="60b61-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60b61-108">-AsJob</span></span>
<span data-ttu-id="60b61-109">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="60b61-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60b61-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60b61-110">-DefaultProfile</span></span>
<span data-ttu-id="60b61-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="60b61-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60b61-112">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="60b61-112">-GatewayVip</span></span>
<span data-ttu-id="60b61-113">Gatewayens VIP-plats för att återställa viss Gateway-instans (t. ex. om det rör sig om Active-Active aktiva gateways.) Som standard återställer gatewayens primära instans om inget värde skickas.</span><span class="sxs-lookup"><span data-stu-id="60b61-113">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="60b61-114">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="60b61-114">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="60b61-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60b61-115">CommonParameters</span></span>
<span data-ttu-id="60b61-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60b61-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60b61-117">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60b61-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60b61-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60b61-118">INPUTS</span></span>

### <span data-ttu-id="60b61-119">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="60b61-119">String</span></span>
<span data-ttu-id="60b61-120">Parametern ' GatewayVip ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="60b61-120">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="60b61-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="60b61-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="60b61-122">Parametern ' VirtualNetworkGateway ' godkänner värdet av typen ' PSVirtualNetworkGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="60b61-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="60b61-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60b61-123">OUTPUTS</span></span>

### <span data-ttu-id="60b61-124">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="60b61-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="60b61-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60b61-125">NOTES</span></span>

## <span data-ttu-id="60b61-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60b61-126">RELATED LINKS</span></span>

[<span data-ttu-id="60b61-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="60b61-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="60b61-128">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="60b61-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="60b61-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="60b61-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="60b61-130">Ändra storlek – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="60b61-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="60b61-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="60b61-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)


