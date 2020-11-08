---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 15f918214a71fe38c850126b31f93d14940fa602
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091661"
---
# <span data-ttu-id="a4bd0-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a4bd0-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="a4bd0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="a4bd0-103">Återställer den virtuella Nätverksgatewayen</span><span class="sxs-lookup"><span data-stu-id="a4bd0-103">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="a4bd0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4bd0-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4bd0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4bd0-105">DESCRIPTION</span></span>
<span data-ttu-id="a4bd0-106">Återställer den virtuella Nätverksgatewayen</span><span class="sxs-lookup"><span data-stu-id="a4bd0-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="a4bd0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4bd0-107">EXAMPLES</span></span>

### <span data-ttu-id="a4bd0-108">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="a4bd0-108">Example 1:</span></span>
```
$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="a4bd0-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4bd0-109">PARAMETERS</span></span>

### <span data-ttu-id="a4bd0-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4bd0-110">-AsJob</span></span>
<span data-ttu-id="a4bd0-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a4bd0-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bd0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4bd0-112">-DefaultProfile</span></span>
<span data-ttu-id="a4bd0-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a4bd0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bd0-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="a4bd0-114">-GatewayVip</span></span>
<span data-ttu-id="a4bd0-115">Gatewayens VIP-plats för att återställa viss Gateway-instans (t. ex. om det rör sig om Active-Active aktiva gateways.) Som standard återställer gatewayens primära instans om inget värde skickas.</span><span class="sxs-lookup"><span data-stu-id="a4bd0-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="a4bd0-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a4bd0-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="a4bd0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4bd0-117">CommonParameters</span></span>
<span data-ttu-id="a4bd0-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4bd0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4bd0-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4bd0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4bd0-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4bd0-120">INPUTS</span></span>

### <span data-ttu-id="a4bd0-121">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a4bd0-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="a4bd0-122">System. String</span><span class="sxs-lookup"><span data-stu-id="a4bd0-122">System.String</span></span>

## <span data-ttu-id="a4bd0-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4bd0-123">OUTPUTS</span></span>

### <span data-ttu-id="a4bd0-124">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a4bd0-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="a4bd0-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4bd0-125">NOTES</span></span>

## <span data-ttu-id="a4bd0-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4bd0-126">RELATED LINKS</span></span>

[<span data-ttu-id="a4bd0-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a4bd0-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a4bd0-128">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a4bd0-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a4bd0-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a4bd0-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a4bd0-130">Ändra storlek – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a4bd0-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a4bd0-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a4bd0-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
