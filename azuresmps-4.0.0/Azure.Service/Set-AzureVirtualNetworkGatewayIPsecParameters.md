---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 150EE0DC-07CD-4E24-AF70-0C1A7BB61433
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b663ced66318335afb1fe4c3bf0e6a1520ede7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099642"
---
# <span data-ttu-id="3dfb7-101">Set-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="3dfb7-101">Set-AzureVirtualNetworkGatewayIPsecParameters</span></span>

## <span data-ttu-id="3dfb7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3dfb7-102">SYNOPSIS</span></span>
<span data-ttu-id="3dfb7-103">Anger IPsec-parametrar för en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="3dfb7-103">Sets IPsec parameters for a virtual network gateway.</span></span>

## <span data-ttu-id="3dfb7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3dfb7-104">SYNTAX</span></span>

```
Set-AzureVirtualNetworkGatewayIPsecParameters -GatewayId <String> -ConnectedEntityId <String>
 [-EncryptionType <String>] [-PfsGroup <String>] [-SADataSizeKilobytes <Int32>] [-SALifetimeSeconds <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3dfb7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3dfb7-105">DESCRIPTION</span></span>
<span data-ttu-id="3dfb7-106">Cmdleten **set-AzureVirtualNetworkGatewayIPsecParameters** anger IPsec-parametrar för en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="3dfb7-106">The **Set-AzureVirtualNetworkGatewayIPsecParameters** cmdlet sets IPsec parameters for a virtual network gateway.</span></span>

## <span data-ttu-id="3dfb7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3dfb7-107">EXAMPLES</span></span>

## <span data-ttu-id="3dfb7-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3dfb7-108">PARAMETERS</span></span>

### <span data-ttu-id="3dfb7-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="3dfb7-109">-ConnectedEntityId</span></span>
<span data-ttu-id="3dfb7-110">Anger ID för en ansluten enhet.</span><span class="sxs-lookup"><span data-stu-id="3dfb7-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="3dfb7-111">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="3dfb7-111">-EncryptionType</span></span>
<span data-ttu-id="3dfb7-112">Anger krypterings typen för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3dfb7-112">Specifies the encryption type for the virtual network gateway.</span></span>
<span data-ttu-id="3dfb7-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3dfb7-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3dfb7-114">Nokryptering</span><span class="sxs-lookup"><span data-stu-id="3dfb7-114">NoEncryption</span></span>
- <span data-ttu-id="3dfb7-115">RequireEncryption</span><span class="sxs-lookup"><span data-stu-id="3dfb7-115">RequireEncryption</span></span>

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

### <span data-ttu-id="3dfb7-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="3dfb7-116">-GatewayId</span></span>
<span data-ttu-id="3dfb7-117">Anger ID för en gateway.</span><span class="sxs-lookup"><span data-stu-id="3dfb7-117">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="3dfb7-118">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="3dfb7-118">-PfsGroup</span></span>
<span data-ttu-id="3dfb7-119">Anger PFS-gruppen (Perfect Forward Secrecy).</span><span class="sxs-lookup"><span data-stu-id="3dfb7-119">Specifies the perfect forward secrecy (PFS) group.</span></span>
<span data-ttu-id="3dfb7-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3dfb7-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3dfb7-121">PFS1</span><span class="sxs-lookup"><span data-stu-id="3dfb7-121">PFS1</span></span>
- <span data-ttu-id="3dfb7-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="3dfb7-122">None</span></span>

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

### <span data-ttu-id="3dfb7-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="3dfb7-123">-Profile</span></span>
<span data-ttu-id="3dfb7-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="3dfb7-124">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3dfb7-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="3dfb7-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3dfb7-126">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="3dfb7-126">-SADataSizeKilobytes</span></span>
<span data-ttu-id="3dfb7-127">Anger storleken i kilobyte för säkerhets associationen (SA).</span><span class="sxs-lookup"><span data-stu-id="3dfb7-127">Specifies the size, in kilobytes, of the security association (SA).</span></span>

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

### <span data-ttu-id="3dfb7-128">-SALifetimeSeconds</span><span class="sxs-lookup"><span data-stu-id="3dfb7-128">-SALifetimeSeconds</span></span>
<span data-ttu-id="3dfb7-129">Anger period i sekunder för säkerhets associationen.</span><span class="sxs-lookup"><span data-stu-id="3dfb7-129">Specifies the period, in seconds, of the security association.</span></span>

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

### <span data-ttu-id="3dfb7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dfb7-130">CommonParameters</span></span>
<span data-ttu-id="3dfb7-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dfb7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dfb7-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dfb7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dfb7-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3dfb7-133">INPUTS</span></span>

## <span data-ttu-id="3dfb7-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3dfb7-134">OUTPUTS</span></span>

## <span data-ttu-id="3dfb7-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3dfb7-135">NOTES</span></span>

## <span data-ttu-id="3dfb7-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3dfb7-136">RELATED LINKS</span></span>

[<span data-ttu-id="3dfb7-137">Get-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="3dfb7-137">Get-AzureVirtualNetworkGatewayIPsecParameters</span></span>](./Get-AzureVirtualNetworkGatewayIPsecParameters.md)


