---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9F9E4639-A557-4BD8-88C2-894F6C848C4A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa54a7bd236bb561b3de4b9c2a3c0a2710deb61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099237"
---
# <span data-ttu-id="e76a3-101">New-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e76a3-101">New-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="e76a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e76a3-102">SYNOPSIS</span></span>
<span data-ttu-id="e76a3-103">skapar en Azure-lokal nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="e76a3-103">creates an Azure local network gateway.</span></span>

## <span data-ttu-id="e76a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e76a3-104">SYNTAX</span></span>

```
New-AzureLocalNetworkGateway -GatewayName <String> -IpAddress <String>
 -AddressSpace <System.Collections.Generic.List`1[System.String]> [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e76a3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e76a3-105">DESCRIPTION</span></span>
<span data-ttu-id="e76a3-106">Cmdleten **New-AzureLocalNetworkGateway** skapar en Azure-lokal gateway.</span><span class="sxs-lookup"><span data-stu-id="e76a3-106">The **New-AzureLocalNetworkGateway** cmdlet creates an Azure local network gateway.</span></span>

## <span data-ttu-id="e76a3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e76a3-107">EXAMPLES</span></span>

## <span data-ttu-id="e76a3-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e76a3-108">PARAMETERS</span></span>

### <span data-ttu-id="e76a3-109">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="e76a3-109">-AddressSpace</span></span>
<span data-ttu-id="e76a3-110">Anger adress utrymmet.</span><span class="sxs-lookup"><span data-stu-id="e76a3-110">Specifies the address space.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e76a3-111">-ASN</span><span class="sxs-lookup"><span data-stu-id="e76a3-111">-Asn</span></span>
<span data-ttu-id="e76a3-112">Anger det autonoma system numret (ASN).</span><span class="sxs-lookup"><span data-stu-id="e76a3-112">Specifies the autonomous system number (ASN).</span></span>

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

### <span data-ttu-id="e76a3-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="e76a3-113">-BgpPeeringAddress</span></span>
<span data-ttu-id="e76a3-114">Anger BGP-peering-adressen (Border Gateway Protocol).</span><span class="sxs-lookup"><span data-stu-id="e76a3-114">Specifies the Border Gateway Protocol (BGP) peering address.</span></span>

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

### <span data-ttu-id="e76a3-115">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="e76a3-115">-GatewayName</span></span>
<span data-ttu-id="e76a3-116">Anger namnet på gatewayen.</span><span class="sxs-lookup"><span data-stu-id="e76a3-116">Specifies the name of the gateway.</span></span>

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

### <span data-ttu-id="e76a3-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="e76a3-117">-IpAddress</span></span>
<span data-ttu-id="e76a3-118">Anger IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="e76a3-118">Specifies the IP address.</span></span>

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

### <span data-ttu-id="e76a3-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="e76a3-119">-PeerWeight</span></span>
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

### <span data-ttu-id="e76a3-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="e76a3-120">-Profile</span></span>
<span data-ttu-id="e76a3-121">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e76a3-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e76a3-122">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e76a3-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e76a3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e76a3-123">CommonParameters</span></span>
<span data-ttu-id="e76a3-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e76a3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e76a3-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e76a3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e76a3-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e76a3-126">INPUTS</span></span>

## <span data-ttu-id="e76a3-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e76a3-127">OUTPUTS</span></span>

## <span data-ttu-id="e76a3-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e76a3-128">NOTES</span></span>

## <span data-ttu-id="e76a3-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e76a3-129">RELATED LINKS</span></span>

[<span data-ttu-id="e76a3-130">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e76a3-130">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="e76a3-131">Remove-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e76a3-131">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)

[<span data-ttu-id="e76a3-132">Reset-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e76a3-132">Reset-AzureLocalNetworkGateway</span></span>](./Reset-AzureLocalNetworkGateway.md)


