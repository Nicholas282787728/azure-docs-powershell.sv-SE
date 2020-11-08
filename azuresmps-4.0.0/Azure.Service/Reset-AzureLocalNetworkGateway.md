---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0E4D44EE-BF28-46FE-B2FA-D35C1651016F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3940a5e6fc69ebee02f3e0de963bc87f790f8860
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093198"
---
# <span data-ttu-id="e7f2b-101">Reset-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e7f2b-101">Reset-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="e7f2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e7f2b-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f2b-103">Återställer en lokal nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="e7f2b-103">Resets a local network gateway.</span></span>

## <span data-ttu-id="e7f2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e7f2b-104">SYNTAX</span></span>

```
Reset-AzureLocalNetworkGateway -GatewayId <String>
 -AddressSpace <System.Collections.Generic.List`1[System.String]> [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e7f2b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e7f2b-105">DESCRIPTION</span></span>
<span data-ttu-id="e7f2b-106">Cmdleten **Reset-AzureLocalNetworkGateway** återställer en lokal nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="e7f2b-106">The **Reset-AzureLocalNetworkGateway** cmdlet resets a local network gateway.</span></span>

## <span data-ttu-id="e7f2b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e7f2b-107">EXAMPLES</span></span>

## <span data-ttu-id="e7f2b-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e7f2b-108">PARAMETERS</span></span>

### <span data-ttu-id="e7f2b-109">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="e7f2b-109">-AddressSpace</span></span>
<span data-ttu-id="e7f2b-110">Anger adress utrymmet.</span><span class="sxs-lookup"><span data-stu-id="e7f2b-110">Specifies the address space.</span></span>

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

### <span data-ttu-id="e7f2b-111">-ASN</span><span class="sxs-lookup"><span data-stu-id="e7f2b-111">-Asn</span></span>
<span data-ttu-id="e7f2b-112">Anger det autonoma system numret (ASN).</span><span class="sxs-lookup"><span data-stu-id="e7f2b-112">Specifies the autonomous system number (ASN).</span></span>

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

### <span data-ttu-id="e7f2b-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="e7f2b-113">-BgpPeeringAddress</span></span>
<span data-ttu-id="e7f2b-114">Anger BGP-peering-adressen (Border Gateway Protocol).</span><span class="sxs-lookup"><span data-stu-id="e7f2b-114">Specifies the Border Gateway Protocol (BGP) peering address.</span></span>

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

### <span data-ttu-id="e7f2b-115">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="e7f2b-115">-GatewayId</span></span>
<span data-ttu-id="e7f2b-116">Anger gatewayens ID.</span><span class="sxs-lookup"><span data-stu-id="e7f2b-116">Specifies the ID of the gateway.</span></span>

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

### <span data-ttu-id="e7f2b-117">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="e7f2b-117">-PeerWeight</span></span>
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

### <span data-ttu-id="e7f2b-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="e7f2b-118">-Profile</span></span>
<span data-ttu-id="e7f2b-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e7f2b-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e7f2b-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e7f2b-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e7f2b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f2b-121">CommonParameters</span></span>
<span data-ttu-id="e7f2b-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7f2b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f2b-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7f2b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f2b-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e7f2b-124">INPUTS</span></span>

## <span data-ttu-id="e7f2b-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e7f2b-125">OUTPUTS</span></span>

## <span data-ttu-id="e7f2b-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e7f2b-126">NOTES</span></span>

## <span data-ttu-id="e7f2b-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e7f2b-127">RELATED LINKS</span></span>

[<span data-ttu-id="e7f2b-128">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e7f2b-128">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="e7f2b-129">New-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e7f2b-129">New-AzureLocalNetworkGateway</span></span>](./New-AzureLocalNetworkGateway.md)

[<span data-ttu-id="e7f2b-130">Remove-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e7f2b-130">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)


