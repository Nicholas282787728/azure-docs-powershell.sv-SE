---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 288812137887e4fc22308bba56a3fbdbeeb28c85
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271531"
---
# <span data-ttu-id="5de47-101">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="5de47-101">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="5de47-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5de47-102">SYNOPSIS</span></span>
<span data-ttu-id="5de47-103">Tar bort standard webbplatsen från en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="5de47-103">Removes the default site from a virtual network gateway.</span></span>

## <span data-ttu-id="5de47-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5de47-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5de47-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5de47-105">DESCRIPTION</span></span>
<span data-ttu-id="5de47-106">Cmdleten **Remove-AzVirtualNetworkGatewayDefaultSite** tar bort den tvingande standard webbplatsen för tunnel trafik från en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="5de47-106">The **Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="5de47-107">Med tvingande tunnlar kan du omdirigera Internet-bundna trafik från virtuella Azure-datorer till det lokala nätverket. Detta gör att du kan kontrol lera och granska trafiken innan den släpps.</span><span class="sxs-lookup"><span data-stu-id="5de47-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="5de47-108">Framtvingad tunnel trafik utförs med en VPN-tunnel (Virtual Private Network). Denna tunnel kräver en standard webbplats, en lokal gateway där all Azure Internet-bunden trafik omdirigeras.</span><span class="sxs-lookup"><span data-stu-id="5de47-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="5de47-109">**Remove-AzVirtualNetworkGatewayDefaultSite** tar bort standard webbplatsen som är tilldelad en gateway.</span><span class="sxs-lookup"><span data-stu-id="5de47-109">**Remove-AzVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="5de47-110">Om du gör det måste du använda Set-AzVirtualNetworkGatewayDefaultSite för att tilldela en ny standard webbplats innan gatewayen kan användas för tvingande tunnel.</span><span class="sxs-lookup"><span data-stu-id="5de47-110">If you do this you will need to use Set-AzVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="5de47-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5de47-111">EXAMPLES</span></span>

### <span data-ttu-id="5de47-112">Exempel 1: ta bort standard webbplatsen som är kopplad till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="5de47-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

<span data-ttu-id="5de47-113">I det här exemplet tas standard webbplatsen för närvarande till en virtuell nätverksgateway som heter ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="5de47-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="5de47-114">Det första kommandot använder **Get-AzVirtualNetworkGateway** för att skapa en objekt referens till gatewayen. Denna objekt referens lagras i en variabel som heter $Gateway.</span><span class="sxs-lookup"><span data-stu-id="5de47-114">The first command uses **Get-AzVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="5de47-115">Det andra kommandot använder **Remove-AzVirtualNetworkGatewayDefaultSite** för att ta bort standard webbplatsen som har tilldelats till den gatewayen.</span><span class="sxs-lookup"><span data-stu-id="5de47-115">The second command then uses **Remove-AzVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="5de47-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5de47-116">PARAMETERS</span></span>

### <span data-ttu-id="5de47-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5de47-117">-DefaultProfile</span></span>
<span data-ttu-id="5de47-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5de47-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5de47-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5de47-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="5de47-120">Anger en objekt referens till den virtuella nätverksgateway som innehåller den standard webbplats som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="5de47-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="5de47-121">Du kan skapa en objekt referens till en virtuell nätverksgateway genom att använda Get-AzVirtualNetworkGateway och ange namnet på gatewayen.</span><span class="sxs-lookup"><span data-stu-id="5de47-121">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="5de47-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5de47-122">CommonParameters</span></span>
<span data-ttu-id="5de47-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5de47-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5de47-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5de47-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5de47-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5de47-125">INPUTS</span></span>

### <span data-ttu-id="5de47-126">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5de47-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="5de47-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5de47-127">OUTPUTS</span></span>

### <span data-ttu-id="5de47-128">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5de47-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="5de47-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5de47-129">NOTES</span></span>

## <span data-ttu-id="5de47-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5de47-130">RELATED LINKS</span></span>

[<span data-ttu-id="5de47-131">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5de47-131">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="5de47-132">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="5de47-132">Set-AzVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzVirtualNetworkGatewayDefaultSite.md)


