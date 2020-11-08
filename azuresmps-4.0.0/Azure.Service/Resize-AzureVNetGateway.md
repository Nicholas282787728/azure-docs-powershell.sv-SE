---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5765F6BD-38BC-451B-85C5-F5D1A5AF2831
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91e5e226cfe4fc4cb27d2df73eb4da4c12045510
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099317"
---
# <span data-ttu-id="a3865-101">Resize-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="a3865-101">Resize-AzureVNetGateway</span></span>

## <span data-ttu-id="a3865-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3865-102">SYNOPSIS</span></span>
<span data-ttu-id="a3865-103">Ändrar storlek på en VPN-gateway.</span><span class="sxs-lookup"><span data-stu-id="a3865-103">Resizes a VPN gateway.</span></span>

## <span data-ttu-id="a3865-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3865-104">SYNTAX</span></span>

```
Resize-AzureVNetGateway -VNetName <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3865-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3865-105">DESCRIPTION</span></span>
<span data-ttu-id="a3865-106">**AzureVNetGateway** cmdlet ändrar storlek på en VPN-gateway (virtuellt privat nätverk) till en annan SKU.</span><span class="sxs-lookup"><span data-stu-id="a3865-106">The **Resize-AzureVNetGateway** cmdlet resizes a virtual network virtual private network (VPN) gateway to a different SKU.</span></span>
<span data-ttu-id="a3865-107">Giltiga SKU: er för en virtuell nätverksgateway är standard, standard och HighPerformance.</span><span class="sxs-lookup"><span data-stu-id="a3865-107">Valid SKUs for a virtual network gateway are Default, Standard, and HighPerformance.</span></span>

## <span data-ttu-id="a3865-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3865-108">EXAMPLES</span></span>

### <span data-ttu-id="a3865-109">Exempel 1: ändra SKU för en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="a3865-109">Example 1: Change the SKU for a virtual network gateway</span></span>
```
PS C:\> Resize-AzureVNetGateway -VNetName "ContosoVN07" -GatewaySKU "HighPerformance"
```

<span data-ttu-id="a3865-110">Det här kommandot ändrar SKU för den virtuella Nätverksgatewayen för det virtuella nätverket som heter ContosoVN07 till HighPerformance.</span><span class="sxs-lookup"><span data-stu-id="a3865-110">This command changes the SKU of the virtual network gateway for the virtual network named ContosoVN07 to HighPerformance.</span></span>

## <span data-ttu-id="a3865-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3865-111">PARAMETERS</span></span>

### <span data-ttu-id="a3865-112">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="a3865-112">-GatewaySKU</span></span>
<span data-ttu-id="a3865-113">Anger den SKU som denna cmdlet ändrar storlek på virtuell nätverksgateway för.</span><span class="sxs-lookup"><span data-stu-id="a3865-113">Specifies the SKU to which this cmdlet resizes virtual network gateway.</span></span>
<span data-ttu-id="a3865-114">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="a3865-114">Valid values are:</span></span> 

- <span data-ttu-id="a3865-115">Vis</span><span class="sxs-lookup"><span data-stu-id="a3865-115">Default</span></span> 
- <span data-ttu-id="a3865-116">Standar</span><span class="sxs-lookup"><span data-stu-id="a3865-116">Standard</span></span> 
- <span data-ttu-id="a3865-117">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="a3865-117">HighPerformance</span></span>

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

### <span data-ttu-id="a3865-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="a3865-118">-Profile</span></span>
<span data-ttu-id="a3865-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="a3865-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a3865-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="a3865-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a3865-121">-VNetName</span><span class="sxs-lookup"><span data-stu-id="a3865-121">-VNetName</span></span>
<span data-ttu-id="a3865-122">Anger det virtuella nätverk där denna cmdlet ändrar storlek på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="a3865-122">Specifies the virtual network in which this cmdlet resizes a virtual network gateway.</span></span>

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

### <span data-ttu-id="a3865-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3865-123">CommonParameters</span></span>
<span data-ttu-id="a3865-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3865-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3865-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3865-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3865-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3865-126">INPUTS</span></span>

## <span data-ttu-id="a3865-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3865-127">OUTPUTS</span></span>

## <span data-ttu-id="a3865-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3865-128">NOTES</span></span>

## <span data-ttu-id="a3865-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3865-129">RELATED LINKS</span></span>

[<span data-ttu-id="a3865-130">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="a3865-130">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="a3865-131">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="a3865-131">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="a3865-132">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="a3865-132">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="a3865-133">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="a3865-133">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="a3865-134">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="a3865-134">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


