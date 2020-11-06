---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/resize-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 0a8a5c4084813bac74ea907575d2bd26c3d8c5f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584060"
---
# <span data-ttu-id="9a3b1-101">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9a3b1-101">Resize-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="9a3b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a3b1-102">SYNOPSIS</span></span>
<span data-ttu-id="9a3b1-103">Ändrar storlek på en befintlig virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-103">Resizes an existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a3b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a3b1-104">SYNTAX</span></span>

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a3b1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a3b1-105">DESCRIPTION</span></span>
<span data-ttu-id="9a3b1-106">Med cmdleten **ändra storlek-AzureRmVirtualNetworkGateway** kan du ändra lagerhållnings enheten (SKU) för en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-106">The **Resize-AzureRmVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="9a3b1-107">SKU: er avgör vilka funktioner en gateway har, inklusive sådant som genomflöde och det högsta antalet IP-tunnlar som tillåts.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="9a3b1-108">Azure har stöd för grundläggande, standard, högpresterande, VpnGw1, VpnGw2, VpnGw3, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ,-SKU: er (kallas ibland för små, medel stora och stora SKU: er).</span><span class="sxs-lookup"><span data-stu-id="9a3b1-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="9a3b1-109">Detaljerad information om funktionerna för varje SKU-typ finns i https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="9a3b1-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>
<span data-ttu-id="9a3b1-110">Kom ihåg att SKU: er skiljer sig från både priser och möjligheter.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="9a3b1-111">Mer information finns i https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="9a3b1-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="9a3b1-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a3b1-112">EXAMPLES</span></span>

### <span data-ttu-id="9a3b1-113">Exempel 1: ändra storleken på en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="9a3b1-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="9a3b1-114">Det här exemplet ändrar storleken på en virtuell nätverksgateway som heter ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="9a3b1-115">Det första kommandot skapar en objekt referens till ContosoVirtualGateway. Denna objekt referens lagras i en variabel som heter $Gateway.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="9a3b1-116">Det andra kommandot använder sedan cmdleten för att **ändra storlek-AzureRmVirtualNetworkGateway** för att ange egenskapen *GatewaySku* till Basic.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-116">The second command then uses the **Resize-AzureRmVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="9a3b1-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a3b1-117">PARAMETERS</span></span>

### <span data-ttu-id="9a3b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a3b1-118">-DefaultProfile</span></span>
<span data-ttu-id="9a3b1-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a3b1-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="9a3b1-120">-GatewaySku</span></span>
<span data-ttu-id="9a3b1-121">Anger den nya typen av Gateway SKU.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="9a3b1-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9a3b1-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9a3b1-123">Basisk</span><span class="sxs-lookup"><span data-stu-id="9a3b1-123">Basic</span></span>
- <span data-ttu-id="9a3b1-124">Standar</span><span class="sxs-lookup"><span data-stu-id="9a3b1-124">Standard</span></span>
- <span data-ttu-id="9a3b1-125">Hög prestanda</span><span class="sxs-lookup"><span data-stu-id="9a3b1-125">High Performance</span></span>
- <span data-ttu-id="9a3b1-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="9a3b1-126">VpnGw1</span></span>
- <span data-ttu-id="9a3b1-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="9a3b1-127">VpnGw2</span></span>
- <span data-ttu-id="9a3b1-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="9a3b1-128">VpnGw3</span></span>
- <span data-ttu-id="9a3b1-129">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="9a3b1-129">VpnGw1AZ</span></span> 
- <span data-ttu-id="9a3b1-130">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="9a3b1-130">VpnGw2AZ</span></span> 
- <span data-ttu-id="9a3b1-131">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="9a3b1-131">VpnGw3AZ</span></span> 
- <span data-ttu-id="9a3b1-132">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="9a3b1-132">ErGw1AZ</span></span> 
- <span data-ttu-id="9a3b1-133">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="9a3b1-133">ErGw2AZ</span></span> 
- <span data-ttu-id="9a3b1-134">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="9a3b1-134">ErGw3AZ</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a3b1-135">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9a3b1-135">-VirtualNetworkGateway</span></span>
<span data-ttu-id="9a3b1-136">Anger en objekt referens till den virtuella nätverksgateway för att ändra storlek.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-136">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="9a3b1-137">Du kan skapa denna objekt referens genom att använda Get-AzureRmVirtualNetworkGateway och ange namnet på gatewayen.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-137">You can create this object reference by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="9a3b1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a3b1-138">CommonParameters</span></span>
<span data-ttu-id="9a3b1-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a3b1-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a3b1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a3b1-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a3b1-141">INPUTS</span></span>

### <span data-ttu-id="9a3b1-142">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9a3b1-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="9a3b1-143">Parametrar: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9a3b1-143">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="9a3b1-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9a3b1-144">System.String</span></span>

## <span data-ttu-id="9a3b1-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a3b1-145">OUTPUTS</span></span>

### <span data-ttu-id="9a3b1-146">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9a3b1-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="9a3b1-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a3b1-147">NOTES</span></span>
<span data-ttu-id="9a3b1-148">Du kan inte ändra storlek från grundläggande/standard-HighPerformance SKU till nya VpnGw1/VpnGw2/VpnGw3 SKU: er.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-148">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="9a3b1-149">Det går ännu inte att ändra storlek från/till VpnGw1AZ/VpnGw2AZ/VpnGw3AZ eller ErGw1AZ/ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-149">Further resize is not allowed from/to VpnGw1AZ/VpnGw2AZ/VpnGw3AZ or ErGw1AZ/ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="9a3b1-150">Storleks ändring tillåts bara inom SKU ' Series ' VpnGw1AZ kan ändras till/från VpnGw2AZ/VpnGw3AZ och ErGw1AZ kan anpassas till/från ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-150">Resize is allowed only within the SKU 'series' e.g VpnGw1AZ can be resized to/from VpnGw2AZ/VpnGw3AZ and ErGw1AZ can be resized to/from ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="9a3b1-151">Läs https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways mer om detta.</span><span class="sxs-lookup"><span data-stu-id="9a3b1-151">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="9a3b1-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a3b1-152">RELATED LINKS</span></span>

[<span data-ttu-id="9a3b1-153">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="9a3b1-153">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="9a3b1-154">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9a3b1-154">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="9a3b1-155">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="9a3b1-155">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


