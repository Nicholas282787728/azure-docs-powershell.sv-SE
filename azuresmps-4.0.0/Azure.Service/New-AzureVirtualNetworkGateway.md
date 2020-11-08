---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A40F3BBB-4DC6-452E-A939-ED610F541EB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7797c916813c985802a0a2f63a5a43e033009a06
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099416"
---
# <span data-ttu-id="2c3c5-101">New-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2c3c5-101">New-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="2c3c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c3c5-102">SYNOPSIS</span></span>
<span data-ttu-id="2c3c5-103">Skapar en virtuell Azure-nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="2c3c5-103">Creates an Azure virtual network gateway.</span></span>

## <span data-ttu-id="2c3c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c3c5-104">SYNTAX</span></span>

```
New-AzureVirtualNetworkGateway -VNetName <String> -GatewayName <String> [-GatewayType <String>]
 [-GatewaySKU <String>] [-Location <String>] [-VnetId <String>] [-Asn <UInt32>] [-PeerWeight <Int32>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2c3c5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c3c5-105">DESCRIPTION</span></span>
<span data-ttu-id="2c3c5-106">Cmdleten **New-AzureVirtualNetworkGateway** skapar en Azure Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="2c3c5-106">The **New-AzureVirtualNetworkGateway** cmdlet creates an Azure virtual network gateway.</span></span>

## <span data-ttu-id="2c3c5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c3c5-107">EXAMPLES</span></span>

## <span data-ttu-id="2c3c5-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c3c5-108">PARAMETERS</span></span>

### <span data-ttu-id="2c3c5-109">-ASN</span><span class="sxs-lookup"><span data-stu-id="2c3c5-109">-Asn</span></span>
<span data-ttu-id="2c3c5-110">Anger det autonoma system numret (ASN).</span><span class="sxs-lookup"><span data-stu-id="2c3c5-110">Specifies the autonomous system number (ASN).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c3c5-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2c3c5-111">-Force</span></span>
<span data-ttu-id="2c3c5-112">Bekräfta inte att Azure Virtual Network Gateway-skapande skapas</span><span class="sxs-lookup"><span data-stu-id="2c3c5-112">Do not confirm Azure Virtual Network Gateway Creation</span></span>

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

### <span data-ttu-id="2c3c5-113">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="2c3c5-113">-GatewayName</span></span>
<span data-ttu-id="2c3c5-114">Anger namnet på gatewayen.</span><span class="sxs-lookup"><span data-stu-id="2c3c5-114">Specifies the name of the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c3c5-115">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="2c3c5-115">-GatewaySKU</span></span>
<span data-ttu-id="2c3c5-116">Anger SKU för den virtuella Nätverksgatewayen som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="2c3c5-116">Specifies the SKU of the virtual network gateway that this cmdlet creates.</span></span>
<span data-ttu-id="2c3c5-117">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="2c3c5-117">Valid values are:</span></span>

- <span data-ttu-id="2c3c5-118">Vis</span><span class="sxs-lookup"><span data-stu-id="2c3c5-118">Default</span></span>
- <span data-ttu-id="2c3c5-119">Standar</span><span class="sxs-lookup"><span data-stu-id="2c3c5-119">Standard</span></span>
- <span data-ttu-id="2c3c5-120">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="2c3c5-120">HighPerformance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c3c5-121">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="2c3c5-121">-GatewayType</span></span>
<span data-ttu-id="2c3c5-122">Anger typen av gateway.</span><span class="sxs-lookup"><span data-stu-id="2c3c5-122">Specifies the type of gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c3c5-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="2c3c5-123">-Location</span></span>
<span data-ttu-id="2c3c5-124">Anger platsen.</span><span class="sxs-lookup"><span data-stu-id="2c3c5-124">Specifies the location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c3c5-125">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="2c3c5-125">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c3c5-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="2c3c5-126">-Profile</span></span>
<span data-ttu-id="2c3c5-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="2c3c5-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2c3c5-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="2c3c5-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c3c5-129">-VnetId</span><span class="sxs-lookup"><span data-stu-id="2c3c5-129">-VnetId</span></span>
<span data-ttu-id="2c3c5-130">Anger ID för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="2c3c5-130">Specifies the ID of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c3c5-131">-VNetName</span><span class="sxs-lookup"><span data-stu-id="2c3c5-131">-VNetName</span></span>
<span data-ttu-id="2c3c5-132">Anger ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="2c3c5-132">Specifies a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c3c5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c3c5-133">CommonParameters</span></span>
<span data-ttu-id="2c3c5-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c3c5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c3c5-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c3c5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c3c5-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c3c5-136">INPUTS</span></span>

## <span data-ttu-id="2c3c5-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c3c5-137">OUTPUTS</span></span>

## <span data-ttu-id="2c3c5-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c3c5-138">NOTES</span></span>

## <span data-ttu-id="2c3c5-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c3c5-139">RELATED LINKS</span></span>

[<span data-ttu-id="2c3c5-140">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2c3c5-140">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="2c3c5-141">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2c3c5-141">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="2c3c5-142">Ändra storlek – AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2c3c5-142">Resize-AzureVirtualNetworkGateway</span></span>](./Resize-AzureVirtualNetworkGateway.md)
