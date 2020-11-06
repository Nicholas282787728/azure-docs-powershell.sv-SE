---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: c5d77619fa5f89c60ce20a097e096709e9a48bae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584067"
---
# <span data-ttu-id="9bf96-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9bf96-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="9bf96-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9bf96-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf96-103">Återställer den virtuella Nätverksgatewayen</span><span class="sxs-lookup"><span data-stu-id="9bf96-103">Resets the Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bf96-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9bf96-104">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bf96-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9bf96-105">DESCRIPTION</span></span>
<span data-ttu-id="9bf96-106">Återställer den virtuella Nätverksgatewayen</span><span class="sxs-lookup"><span data-stu-id="9bf96-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="9bf96-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9bf96-107">EXAMPLES</span></span>

### <span data-ttu-id="9bf96-108">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="9bf96-108">Example 1:</span></span>
```
$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="9bf96-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9bf96-109">PARAMETERS</span></span>

### <span data-ttu-id="9bf96-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9bf96-110">-AsJob</span></span>
<span data-ttu-id="9bf96-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9bf96-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9bf96-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf96-112">-DefaultProfile</span></span>
<span data-ttu-id="9bf96-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9bf96-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bf96-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="9bf96-114">-GatewayVip</span></span>
<span data-ttu-id="9bf96-115">Gatewayens VIP-plats för att återställa viss Gateway-instans (t. ex. om det rör sig om Active-Active aktiva gateways.) Som standard återställer gatewayens primära instans om inget värde skickas.</span><span class="sxs-lookup"><span data-stu-id="9bf96-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="9bf96-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9bf96-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="9bf96-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf96-117">CommonParameters</span></span>
<span data-ttu-id="9bf96-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bf96-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf96-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bf96-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf96-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9bf96-120">INPUTS</span></span>

### <span data-ttu-id="9bf96-121">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9bf96-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="9bf96-122">Parametrar: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9bf96-122">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="9bf96-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9bf96-123">System.String</span></span>
<span data-ttu-id="9bf96-124">Parametrar: GatewayVip (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9bf96-124">Parameters: GatewayVip (ByValue)</span></span>

## <span data-ttu-id="9bf96-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9bf96-125">OUTPUTS</span></span>

### <span data-ttu-id="9bf96-126">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9bf96-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="9bf96-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9bf96-127">NOTES</span></span>

## <span data-ttu-id="9bf96-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9bf96-128">RELATED LINKS</span></span>

[<span data-ttu-id="9bf96-129">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9bf96-129">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="9bf96-130">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9bf96-130">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="9bf96-131">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9bf96-131">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="9bf96-132">Ändra storlek – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9bf96-132">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="9bf96-133">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9bf96-133">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


