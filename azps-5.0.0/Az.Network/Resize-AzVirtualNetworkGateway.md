---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: dd48af6a0f20cafea5911adb629a83323faa94a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325241"
---
# <span data-ttu-id="7a6e2-101">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a6e2-101">Resize-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="7a6e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a6e2-102">SYNOPSIS</span></span>
<span data-ttu-id="7a6e2-103">Ändrar storlek på en befintlig virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-103">Resizes an existing virtual network gateway.</span></span>

## <span data-ttu-id="7a6e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a6e2-104">SYNTAX</span></span>

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a6e2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a6e2-105">DESCRIPTION</span></span>
<span data-ttu-id="7a6e2-106">Med cmdleten **ändra storlek-AzVirtualNetworkGateway** kan du ändra lagerhållnings enheten (SKU) för en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-106">The **Resize-AzVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="7a6e2-107">SKU: er avgör vilka funktioner en gateway har, inklusive sådant som genomflöde och det högsta antalet IP-tunnlar som tillåts.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="7a6e2-108">Azure har stöd för grundläggande, standard, högpresterande, VpnGw1, VpnGw2, VpnGw3, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ,-SKU: er (kallas ibland för små, medel stora och stora SKU: er).</span><span class="sxs-lookup"><span data-stu-id="7a6e2-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="7a6e2-109">Detaljerad information om funktionerna för varje SKU-typ finns i https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="7a6e2-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>
<span data-ttu-id="7a6e2-110">Kom ihåg att SKU: er skiljer sig från både priser och möjligheter.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="7a6e2-111">Mer information finns i https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="7a6e2-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="7a6e2-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a6e2-112">EXAMPLES</span></span>

### <span data-ttu-id="7a6e2-113">Exempel 1: ändra storleken på en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="7a6e2-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="7a6e2-114">Det här exemplet ändrar storleken på en virtuell nätverksgateway som heter ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="7a6e2-115">Det första kommandot skapar en objekt referens till ContosoVirtualGateway. Denna objekt referens lagras i en variabel som heter $Gateway.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="7a6e2-116">Det andra kommandot använder sedan cmdleten för att **ändra storlek-AzVirtualNetworkGateway** för att ange egenskapen *GatewaySku* till Basic.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-116">The second command then uses the **Resize-AzVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="7a6e2-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a6e2-117">PARAMETERS</span></span>

### <span data-ttu-id="7a6e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a6e2-118">-DefaultProfile</span></span>
<span data-ttu-id="7a6e2-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a6e2-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="7a6e2-120">-GatewaySku</span></span>
<span data-ttu-id="7a6e2-121">Anger den nya typen av Gateway SKU.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="7a6e2-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7a6e2-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7a6e2-123">Basisk</span><span class="sxs-lookup"><span data-stu-id="7a6e2-123">Basic</span></span>
- <span data-ttu-id="7a6e2-124">Standar</span><span class="sxs-lookup"><span data-stu-id="7a6e2-124">Standard</span></span>
- <span data-ttu-id="7a6e2-125">Hög prestanda</span><span class="sxs-lookup"><span data-stu-id="7a6e2-125">High Performance</span></span>
- <span data-ttu-id="7a6e2-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="7a6e2-126">VpnGw1</span></span>
- <span data-ttu-id="7a6e2-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="7a6e2-127">VpnGw2</span></span>
- <span data-ttu-id="7a6e2-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="7a6e2-128">VpnGw3</span></span>
- <span data-ttu-id="7a6e2-129">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="7a6e2-129">VpnGw1AZ</span></span> 
- <span data-ttu-id="7a6e2-130">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="7a6e2-130">VpnGw2AZ</span></span> 
- <span data-ttu-id="7a6e2-131">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="7a6e2-131">VpnGw3AZ</span></span> 
- <span data-ttu-id="7a6e2-132">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="7a6e2-132">ErGw1AZ</span></span> 
- <span data-ttu-id="7a6e2-133">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="7a6e2-133">ErGw2AZ</span></span> 
- <span data-ttu-id="7a6e2-134">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="7a6e2-134">ErGw3AZ</span></span> 

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

### <span data-ttu-id="7a6e2-135">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a6e2-135">-VirtualNetworkGateway</span></span>
<span data-ttu-id="7a6e2-136">Anger en objekt referens till den virtuella nätverksgateway för att ändra storlek.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-136">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="7a6e2-137">Du kan skapa denna objekt referens genom att använda Get-AzVirtualNetworkGateway och ange namnet på gatewayen.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-137">You can create this object reference by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="7a6e2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a6e2-138">CommonParameters</span></span>
<span data-ttu-id="7a6e2-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a6e2-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a6e2-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a6e2-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a6e2-141">INPUTS</span></span>

### <span data-ttu-id="7a6e2-142">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a6e2-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="7a6e2-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7a6e2-143">System.String</span></span>

## <span data-ttu-id="7a6e2-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a6e2-144">OUTPUTS</span></span>

### <span data-ttu-id="7a6e2-145">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a6e2-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7a6e2-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a6e2-146">NOTES</span></span>
<span data-ttu-id="7a6e2-147">Du kan inte ändra storlek från grundläggande/standard-HighPerformance SKU till nya VpnGw1/VpnGw2/VpnGw3 SKU: er.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-147">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="7a6e2-148">Det går ännu inte att ändra storlek från/till VpnGw1AZ/VpnGw2AZ/VpnGw3AZ eller ErGw1AZ/ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-148">Further resize is not allowed from/to VpnGw1AZ/VpnGw2AZ/VpnGw3AZ or ErGw1AZ/ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="7a6e2-149">Storleks ändring tillåts bara inom SKU ' Series ' VpnGw1AZ kan ändras till/från VpnGw2AZ/VpnGw3AZ och ErGw1AZ kan anpassas till/från ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-149">Resize is allowed only within the SKU 'series' e.g VpnGw1AZ can be resized to/from VpnGw2AZ/VpnGw3AZ and ErGw1AZ can be resized to/from ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="7a6e2-150">Läs https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways mer om detta.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-150">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="7a6e2-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a6e2-151">RELATED LINKS</span></span>

[<span data-ttu-id="7a6e2-152">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a6e2-152">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="7a6e2-153">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a6e2-153">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="7a6e2-154">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a6e2-154">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="7a6e2-155">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a6e2-155">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="7a6e2-156">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a6e2-156">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

[<span data-ttu-id="7a6e2-157">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="7a6e2-157">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

[<span data-ttu-id="7a6e2-158">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="7a6e2-158">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)
