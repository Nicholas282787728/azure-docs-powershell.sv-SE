---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 59f4a96c324a9743c876cf987e1347bbe0c8d946
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917982"
---
# <span data-ttu-id="15875-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="15875-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="15875-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15875-102">SYNOPSIS</span></span>
<span data-ttu-id="15875-103">Återställer den virtuella Nätverksgatewayen</span><span class="sxs-lookup"><span data-stu-id="15875-103">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="15875-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15875-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15875-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15875-105">DESCRIPTION</span></span>
<span data-ttu-id="15875-106">Återställer den virtuella Nätverksgatewayen</span><span class="sxs-lookup"><span data-stu-id="15875-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="15875-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15875-107">EXAMPLES</span></span>

### <span data-ttu-id="15875-108">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="15875-108">Example 1:</span></span>
```
$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="15875-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15875-109">PARAMETERS</span></span>

### <span data-ttu-id="15875-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15875-110">-AsJob</span></span>
<span data-ttu-id="15875-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="15875-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15875-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15875-112">-DefaultProfile</span></span>
<span data-ttu-id="15875-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="15875-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15875-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="15875-114">-GatewayVip</span></span>
<span data-ttu-id="15875-115">Gatewayens VIP-plats för att återställa viss Gateway-instans (t. ex. om det rör sig om Active-Active aktiva gateways.) Som standard återställer gatewayens primära instans om inget värde skickas.</span><span class="sxs-lookup"><span data-stu-id="15875-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="15875-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="15875-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="15875-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15875-117">CommonParameters</span></span>
<span data-ttu-id="15875-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15875-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15875-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15875-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15875-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15875-120">INPUTS</span></span>

### <span data-ttu-id="15875-121">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="15875-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="15875-122">System. String</span><span class="sxs-lookup"><span data-stu-id="15875-122">System.String</span></span>

## <span data-ttu-id="15875-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15875-123">OUTPUTS</span></span>

### <span data-ttu-id="15875-124">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="15875-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="15875-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15875-125">NOTES</span></span>

## <span data-ttu-id="15875-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15875-126">RELATED LINKS</span></span>

[<span data-ttu-id="15875-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="15875-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="15875-128">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="15875-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="15875-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="15875-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="15875-130">Ändra storlek – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="15875-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="15875-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="15875-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
