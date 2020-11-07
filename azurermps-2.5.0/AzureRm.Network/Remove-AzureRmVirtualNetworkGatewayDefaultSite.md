---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
ms.openlocfilehash: ded608261981073ef5544df2b64e99171eef7710
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929289"
---
# <span data-ttu-id="72723-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="72723-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="72723-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72723-102">SYNOPSIS</span></span>
<span data-ttu-id="72723-103">Tar bort standard webbplatsen från en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="72723-103">Removes the default site from a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72723-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72723-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72723-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72723-105">DESCRIPTION</span></span>
<span data-ttu-id="72723-106">Cmdleten **Remove-AzureRmVirtualNetworkGatewayDefaultSite** tar bort den tvingande standard webbplatsen för tunnel trafik från en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="72723-106">The **Remove-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="72723-107">Med tvingande tunnlar kan du omdirigera Internet-bundna trafik från virtuella Azure-datorer till det lokala nätverket. Detta gör att du kan kontrol lera och granska trafiken innan den släpps.</span><span class="sxs-lookup"><span data-stu-id="72723-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="72723-108">Framtvingad tunnel trafik utförs med en VPN-tunnel (Virtual Private Network). Denna tunnel kräver en standard webbplats, en lokal gateway där all Azure Internet-bunden trafik omdirigeras.</span><span class="sxs-lookup"><span data-stu-id="72723-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>

<span data-ttu-id="72723-109">**Remove-AzureRmVirtualNetworkGatewayDefaultSite** tar bort standard webbplatsen som är tilldelad en gateway.</span><span class="sxs-lookup"><span data-stu-id="72723-109">**Remove-AzureRmVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="72723-110">Om du gör det måste du använda Set-AzureRmVirtualNetworkGatewayDefaultSite för att tilldela en ny standard webbplats innan gatewayen kan användas för tvingande tunnel.</span><span class="sxs-lookup"><span data-stu-id="72723-110">If you do this you will need to use Set-AzureRmVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="72723-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72723-111">EXAMPLES</span></span>

### <span data-ttu-id="72723-112">Exempel 1: ta bort standard webbplatsen som är kopplad till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="72723-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworknGateway $Gateway
```

<span data-ttu-id="72723-113">I det här exemplet tas standard webbplatsen för närvarande till en virtuell nätverksgateway som heter ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="72723-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="72723-114">Det första kommandot använder **Get-AzureRmVirtualNetworkGateway** för att skapa en objekt referens till gatewayen. Denna objekt referens lagras i en variabel som heter $Gateway.</span><span class="sxs-lookup"><span data-stu-id="72723-114">The first command uses **Get-AzureRmVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="72723-115">Det andra kommandot använder **Remove-AzureRmVirtualNetworkGatewayDefaultSite** för att ta bort standard webbplatsen som har tilldelats till den gatewayen.</span><span class="sxs-lookup"><span data-stu-id="72723-115">The second command then uses **Remove-AzureRmVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="72723-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72723-116">PARAMETERS</span></span>

### <span data-ttu-id="72723-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72723-117">-DefaultProfile</span></span>
<span data-ttu-id="72723-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="72723-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72723-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="72723-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="72723-120">Anger en objekt referens till den virtuella nätverksgateway som innehåller den standard webbplats som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="72723-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="72723-121">Du kan skapa en objekt referens till en virtuell nätverksgateway genom att använda Get-AzureRmVirtualNetworkGateway och ange namnet på gatewayen.</span><span class="sxs-lookup"><span data-stu-id="72723-121">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="72723-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72723-122">CommonParameters</span></span>
<span data-ttu-id="72723-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72723-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72723-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72723-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72723-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72723-125">INPUTS</span></span>

###  
<span data-ttu-id="72723-126">Denna cmdlet accepterar pipeline-instanser av **Microsoft. Azure. commands. Network. Models. PSVirtualNetworkGateway** -objektet.</span><span class="sxs-lookup"><span data-stu-id="72723-126">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="72723-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72723-127">OUTPUTS</span></span>

###  
<span data-ttu-id="72723-128">Denna cmdlet ändrar befintliga instanser av **Microsoft. Azure. commands. Network. Models. PSVirtualNetworkGateway** -objektet.</span><span class="sxs-lookup"><span data-stu-id="72723-128">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="72723-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72723-129">NOTES</span></span>

## <span data-ttu-id="72723-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72723-130">RELATED LINKS</span></span>

[<span data-ttu-id="72723-131">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="72723-131">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="72723-132">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="72723-132">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzureRmVirtualNetworkGatewayDefaultSite.md)


