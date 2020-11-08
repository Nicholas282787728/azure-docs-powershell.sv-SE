---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 36DA2BF9-091E-4A2C-B5E1-07B4D2E482FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: b73626681e4d089b3b4f20c72080159c31b1bf81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099417"
---
# <span data-ttu-id="540a6-101">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="540a6-101">New-AzureVNetGateway</span></span>

## <span data-ttu-id="540a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="540a6-102">SYNOPSIS</span></span>
<span data-ttu-id="540a6-103">Skapar en VPN-gateway i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="540a6-103">Creates a VPN gateway in a virtual network.</span></span>

## <span data-ttu-id="540a6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="540a6-104">SYNTAX</span></span>

```
New-AzureVNetGateway -VNetName <String> [-GatewayType <String>] [-GatewaySKU <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="540a6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="540a6-105">DESCRIPTION</span></span>
<span data-ttu-id="540a6-106">Cmdleten **New-AzureVNetGateway** skapar en gateway för virtuella privata nätverk (VPN) i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="540a6-106">The **New-AzureVNetGateway** cmdlet creates a virtual private network (VPN) gateway in a virtual network.</span></span>
<span data-ttu-id="540a6-107">Du kan också ange gatewayens SKU: standard, standard eller HighPerformance.</span><span class="sxs-lookup"><span data-stu-id="540a6-107">You can also specify the SKU of the gateway, either Default, Standard, or HighPerformance.</span></span>
<span data-ttu-id="540a6-108">Du kan ange typen, antingen StaticRouting eller DynamicRouting.</span><span class="sxs-lookup"><span data-stu-id="540a6-108">You can specify the type, either StaticRouting or DynamicRouting.</span></span>

## <span data-ttu-id="540a6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="540a6-109">EXAMPLES</span></span>

### <span data-ttu-id="540a6-110">Exempel 1: skapa en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="540a6-110">Example 1: Create a virtual network gateway</span></span>
```
PS C:\> New-AzureVNetGateway -VNetName "ContosoVN07" -GatewayType "DynamicRouting" -GatewaySKU "Default"
```

<span data-ttu-id="540a6-111">Det här kommandot skapar en virtuell nätverksgateway för det virtuella nätverket med namnet ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="540a6-111">This command creates a virtual network gateway for the virtual network named ContosoVN07.</span></span>
<span data-ttu-id="540a6-112">Gatewayen är standard-SKU och använder dynamisk routing.</span><span class="sxs-lookup"><span data-stu-id="540a6-112">The gateway is the Default SKU and uses dynamic routing.</span></span>

## <span data-ttu-id="540a6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="540a6-113">PARAMETERS</span></span>

### <span data-ttu-id="540a6-114">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="540a6-114">-GatewaySKU</span></span>
<span data-ttu-id="540a6-115">Anger SKU för den virtuella Nätverksgatewayen som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="540a6-115">Specifies the SKU of the virtual network gateway that this cmdlet creates.</span></span>
<span data-ttu-id="540a6-116">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="540a6-116">Valid values are:</span></span> 

- <span data-ttu-id="540a6-117">Vis</span><span class="sxs-lookup"><span data-stu-id="540a6-117">Default</span></span> 
- <span data-ttu-id="540a6-118">Standar</span><span class="sxs-lookup"><span data-stu-id="540a6-118">Standard</span></span> 
- <span data-ttu-id="540a6-119">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="540a6-119">HighPerformance</span></span>

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

### <span data-ttu-id="540a6-120">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="540a6-120">-GatewayType</span></span>
<span data-ttu-id="540a6-121">Anger den typ av gateway som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="540a6-121">Specifies the type of gateway that this cmdlet creates.</span></span>
<span data-ttu-id="540a6-122">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="540a6-122">Valid values are:</span></span> 

- <span data-ttu-id="540a6-123">StaticRouting</span><span class="sxs-lookup"><span data-stu-id="540a6-123">StaticRouting</span></span> 
- <span data-ttu-id="540a6-124">DynamicRouting</span><span class="sxs-lookup"><span data-stu-id="540a6-124">DynamicRouting</span></span>

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

### <span data-ttu-id="540a6-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="540a6-125">-Profile</span></span>
<span data-ttu-id="540a6-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="540a6-126">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="540a6-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="540a6-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="540a6-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="540a6-128">-VNetName</span></span>
<span data-ttu-id="540a6-129">Anger det virtuella nätverk där denna cmdlet lägger till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="540a6-129">Specifies the virtual network in which this cmdlet adds a virtual network gateway.</span></span>

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

### <span data-ttu-id="540a6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="540a6-130">CommonParameters</span></span>
<span data-ttu-id="540a6-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="540a6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="540a6-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="540a6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="540a6-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="540a6-133">INPUTS</span></span>

## <span data-ttu-id="540a6-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="540a6-134">OUTPUTS</span></span>

## <span data-ttu-id="540a6-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="540a6-135">NOTES</span></span>

## <span data-ttu-id="540a6-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="540a6-136">RELATED LINKS</span></span>

[<span data-ttu-id="540a6-137">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="540a6-137">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="540a6-138">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="540a6-138">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="540a6-139">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="540a6-139">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="540a6-140">Ändra storlek – AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="540a6-140">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="540a6-141">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="540a6-141">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


