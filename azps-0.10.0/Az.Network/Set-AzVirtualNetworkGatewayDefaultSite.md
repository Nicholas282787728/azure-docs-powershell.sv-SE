---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 560053ca6b5e49ffcef8dbb6ee4b0ba32f3ed276
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924146"
---
# <span data-ttu-id="691c2-101">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="691c2-101">Set-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="691c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="691c2-102">SYNOPSIS</span></span>
<span data-ttu-id="691c2-103">Anger standard platsen för en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="691c2-103">Sets the default site for a virtual network gateway.</span></span>

## <span data-ttu-id="691c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="691c2-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="691c2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="691c2-105">DESCRIPTION</span></span>
<span data-ttu-id="691c2-106">Cmdleten **set-AzVirtualNetworkGatewayDefaultSite** tilldelar en standard plats för tvingande tunnel till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="691c2-106">The **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="691c2-107">Med tvingande tunnlar kan du omdirigera Internet-bundna trafik från virtuella Azure-datorer till det lokala nätverket. Detta gör att du kan kontrol lera och granska trafiken innan den släpps.</span><span class="sxs-lookup"><span data-stu-id="691c2-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="691c2-108">Framtvingad tunnel trafik utförs med en VPN-tunnel (Virtual Private Network). Denna tunnel kräver en standard webbplats, en lokal gateway där all Azure Internet-bunden trafik omdirigeras.</span><span class="sxs-lookup"><span data-stu-id="691c2-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="691c2-109">**Set-AzVirtualNetworkGatewayDefaultSite** ger dig ett sätt att ändra standard webbplatsen som är tilldelad en gateway.</span><span class="sxs-lookup"><span data-stu-id="691c2-109">**Set-AzVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="691c2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="691c2-110">EXAMPLES</span></span>

### <span data-ttu-id="691c2-111">Exempel 1: tilldela en standard webbplats till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="691c2-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="691c2-112">I det här exemplet tilldelas en standard webbplats till en virtuell nätverksgateway med namnet ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="691c2-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="691c2-113">Det första kommandot skapar en objekt referens till en lokal gateway som heter ContosoLocalGateway.</span><span class="sxs-lookup"><span data-stu-id="691c2-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="691c2-114">Den här objekt referensen som lagras i variabeln som heter $LocalGateway representerar den gateway som ska konfigureras som standard webbplats</span><span class="sxs-lookup"><span data-stu-id="691c2-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site</span></span>

<span data-ttu-id="691c2-115">.</span><span class="sxs-lookup"><span data-stu-id="691c2-115">.</span></span>
<span data-ttu-id="691c2-116">Det andra kommandot skapar sedan en objekt referens till den virtuella Nätverksgatewayen och lagrar resultatet i variabeln som heter $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="691c2-116">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>

<span data-ttu-id="691c2-117">I det tredje kommandot används cmdleten **set-AzVirtualNetworkGatewayDefaultSite** för att koppla standard platsen till ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="691c2-117">The third command uses the **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="691c2-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="691c2-118">PARAMETERS</span></span>

### <span data-ttu-id="691c2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="691c2-119">-DefaultProfile</span></span>
<span data-ttu-id="691c2-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="691c2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="691c2-121">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="691c2-121">-GatewayDefaultSite</span></span>
<span data-ttu-id="691c2-122">Anger en objekt referens till den lokala Nätverksgatewayen som ska tilldelas som standard webbplats för det angivna virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="691c2-122">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="691c2-123">Du kan använda Get-AzLocalNetworkGateway cmdlet för att skapa en objekt referens till en lokal gateway.</span><span class="sxs-lookup"><span data-stu-id="691c2-123">You can use the Get-AzLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="691c2-124">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="691c2-124">-VirtualNetworkGateway</span></span>
<span data-ttu-id="691c2-125">Anger en objekt referens till den virtuella Nätverksgatewayen där standard webbplatsen tilldelas.</span><span class="sxs-lookup"><span data-stu-id="691c2-125">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="691c2-126">Du kan skapa en objekt referens till en virtuell nätverksgateway genom att använda **Get-AzVirtualNetworkGateway** och ange namnet på gatewayen.</span><span class="sxs-lookup"><span data-stu-id="691c2-126">You can create an object reference to a virtual network gateway by using the **Get-AzVirtualNetworkGateway** and specifying the name of the gateway.</span></span>

<span data-ttu-id="691c2-127">Variabeln $VirtualGateway kan sedan användas som parameter värde för parametern *VirtualNetworkGateway* :</span><span class="sxs-lookup"><span data-stu-id="691c2-127">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="691c2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="691c2-128">CommonParameters</span></span>
<span data-ttu-id="691c2-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="691c2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="691c2-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="691c2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="691c2-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="691c2-131">INPUTS</span></span>

###  
<span data-ttu-id="691c2-132">Denna cmdlet accepterar pipeline-instanser av **Microsoft. Azure. commands. Network. Models. PSVirtualNetworkGateway** -objektet.</span><span class="sxs-lookup"><span data-stu-id="691c2-132">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="691c2-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="691c2-133">OUTPUTS</span></span>

###  
<span data-ttu-id="691c2-134">Denna cmdlet ändrar befintliga instanser av **Microsoft. Azure. commands. Network. Models. PSVirtualNetworkGateway** -objektet.</span><span class="sxs-lookup"><span data-stu-id="691c2-134">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="691c2-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="691c2-135">NOTES</span></span>

## <span data-ttu-id="691c2-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="691c2-136">RELATED LINKS</span></span>

[<span data-ttu-id="691c2-137">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="691c2-137">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="691c2-138">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="691c2-138">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="691c2-139">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="691c2-139">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzVirtualNetworkGatewayDefaultSite.md)

