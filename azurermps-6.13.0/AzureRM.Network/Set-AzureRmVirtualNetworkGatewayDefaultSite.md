---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 9c0eec0f38929efe188d8ab0ba8e30d31a16b717
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576149"
---
# <span data-ttu-id="a1fd7-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="a1fd7-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="a1fd7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1fd7-102">SYNOPSIS</span></span>
<span data-ttu-id="a1fd7-103">Anger standard platsen för en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="a1fd7-103">Sets the default site for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1fd7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1fd7-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1fd7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1fd7-105">DESCRIPTION</span></span>
<span data-ttu-id="a1fd7-106">Cmdleten **set-AzureRmVirtualNetworkGatewayDefaultSite** tilldelar en standard plats för tvingande tunnel till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="a1fd7-106">The **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="a1fd7-107">Med tvingande tunnlar kan du omdirigera Internet-bundna trafik från virtuella Azure-datorer till det lokala nätverket. Detta gör att du kan kontrol lera och granska trafiken innan den släpps.</span><span class="sxs-lookup"><span data-stu-id="a1fd7-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="a1fd7-108">Framtvingad tunnel trafik utförs med en VPN-tunnel (Virtual Private Network). Denna tunnel kräver en standard webbplats, en lokal gateway där all Azure Internet-bunden trafik omdirigeras.</span><span class="sxs-lookup"><span data-stu-id="a1fd7-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="a1fd7-109">**Set-AzureRmVirtualNetworkGatewayDefaultSite** ger dig ett sätt att ändra standard webbplatsen som är tilldelad en gateway.</span><span class="sxs-lookup"><span data-stu-id="a1fd7-109">**Set-AzureRmVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="a1fd7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1fd7-110">EXAMPLES</span></span>

### <span data-ttu-id="a1fd7-111">Exempel 1: tilldela en standard webbplats till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="a1fd7-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzureRmLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="a1fd7-112">I det här exemplet tilldelas en standard webbplats till en virtuell nätverksgateway med namnet ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="a1fd7-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="a1fd7-113">Det första kommandot skapar en objekt referens till en lokal gateway som heter ContosoLocalGateway.</span><span class="sxs-lookup"><span data-stu-id="a1fd7-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="a1fd7-114">Denna objekt referens som lagras i variabeln som heter $LocalGateway representerar den gateway som ska konfigureras som standard webbplats.</span><span class="sxs-lookup"><span data-stu-id="a1fd7-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site .</span></span>
<span data-ttu-id="a1fd7-115">Det andra kommandot skapar sedan en objekt referens till den virtuella Nätverksgatewayen och lagrar resultatet i variabeln som heter $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="a1fd7-115">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>
<span data-ttu-id="a1fd7-116">I det tredje kommandot används cmdleten **set-AzureRmVirtualNetworkGatewayDefaultSite** för att koppla standard platsen till ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="a1fd7-116">The third command uses the **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="a1fd7-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1fd7-117">PARAMETERS</span></span>

### <span data-ttu-id="a1fd7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1fd7-118">-DefaultProfile</span></span>
<span data-ttu-id="a1fd7-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a1fd7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1fd7-120">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="a1fd7-120">-GatewayDefaultSite</span></span>
<span data-ttu-id="a1fd7-121">Anger en objekt referens till den lokala Nätverksgatewayen som ska tilldelas som standard webbplats för det angivna virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="a1fd7-121">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="a1fd7-122">Du kan använda Get-AzureRmLocalNetworkGateway cmdlet för att skapa en objekt referens till en lokal gateway.</span><span class="sxs-lookup"><span data-stu-id="a1fd7-122">You can use the Get-AzureRmLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1fd7-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a1fd7-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="a1fd7-124">Anger en objekt referens till den virtuella Nätverksgatewayen där standard webbplatsen tilldelas.</span><span class="sxs-lookup"><span data-stu-id="a1fd7-124">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="a1fd7-125">Du kan skapa en objekt referens till en virtuell nätverksgateway genom att använda **Get-AzureRmVirtualNetworkGateway** och ange namnet på gatewayen.</span><span class="sxs-lookup"><span data-stu-id="a1fd7-125">You can create an object reference to a virtual network gateway by using the **Get-AzureRmVirtualNetworkGateway** and specifying the name of the gateway.</span></span>
<span data-ttu-id="a1fd7-126">Variabeln $VirtualGateway kan sedan användas som parameter värde för parametern *VirtualNetworkGateway* :</span><span class="sxs-lookup"><span data-stu-id="a1fd7-126">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="a1fd7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1fd7-127">CommonParameters</span></span>
<span data-ttu-id="a1fd7-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1fd7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1fd7-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1fd7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1fd7-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1fd7-130">INPUTS</span></span>

### <span data-ttu-id="a1fd7-131">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a1fd7-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="a1fd7-132">Parametrar: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a1fd7-132">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="a1fd7-133">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a1fd7-133">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="a1fd7-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1fd7-134">OUTPUTS</span></span>

### <span data-ttu-id="a1fd7-135">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a1fd7-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="a1fd7-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1fd7-136">NOTES</span></span>

## <span data-ttu-id="a1fd7-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1fd7-137">RELATED LINKS</span></span>

[<span data-ttu-id="a1fd7-138">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a1fd7-138">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="a1fd7-139">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a1fd7-139">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="a1fd7-140">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="a1fd7-140">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzureRmVirtualNetworkGatewayDefaultSite.md)


