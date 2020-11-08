---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C85576C1-182B-467E-9620-A475728E20D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3715b07c66d76c824e684976f18de4ecea64cdb1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099266"
---
# <span data-ttu-id="e2c1d-101">Set-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="e2c1d-101">Set-AzureVNetGatewayIPsecParameters</span></span>

## <span data-ttu-id="e2c1d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2c1d-102">SYNOPSIS</span></span>
<span data-ttu-id="e2c1d-103">Anger IPsec-parametrar för anslutningen mellan en virtuell nätverksgateway och en lokal nätverks webbplats.</span><span class="sxs-lookup"><span data-stu-id="e2c1d-103">Sets IPsec parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="e2c1d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2c1d-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-EncryptionType <String>] [-PfsGroup <String>] [-SADataSizeKilobytes <Int32>] [-SALifetimeSeconds <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e2c1d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2c1d-105">DESCRIPTION</span></span>
<span data-ttu-id="e2c1d-106">Cmdleten **set-AzureVNetGatewayIPsecParameters** anger IPSec-(Internet Protocol Security) och IKE-parametrar (Internet Key Exchange) för anslutningen mellan en virtuell nätverksgateway och en lokal nätverks webbplats.</span><span class="sxs-lookup"><span data-stu-id="e2c1d-106">The **Set-AzureVNetGatewayIPsecParameters** cmdlet sets Internet Protocol security (IPsec) and Internet Key Exchange (IKE) parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="e2c1d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2c1d-107">EXAMPLES</span></span>

## <span data-ttu-id="e2c1d-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2c1d-108">PARAMETERS</span></span>

### <span data-ttu-id="e2c1d-109">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="e2c1d-109">-EncryptionType</span></span>
<span data-ttu-id="e2c1d-110">Anger krypterings typen för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2c1d-110">Specifies the encryption type for the virtual network gateway.</span></span>
<span data-ttu-id="e2c1d-111">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="e2c1d-111">Valid values are:</span></span> 

- <span data-ttu-id="e2c1d-112">Nokryptering</span><span class="sxs-lookup"><span data-stu-id="e2c1d-112">NoEncryption</span></span> 
- <span data-ttu-id="e2c1d-113">RequireEncryption</span><span class="sxs-lookup"><span data-stu-id="e2c1d-113">RequireEncryption</span></span>

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

### <span data-ttu-id="e2c1d-114">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="e2c1d-114">-LocalNetworkSiteName</span></span>
<span data-ttu-id="e2c1d-115">Anger namnet på den lokala nätverks plats anslutningen som den här cmdleten konfigurerar IPsec-och IKE-parametrarna på.</span><span class="sxs-lookup"><span data-stu-id="e2c1d-115">Specifies the name of the local network site connection on which this cmdlet configures the IPsec and IKE parameters.</span></span>

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

### <span data-ttu-id="e2c1d-116">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="e2c1d-116">-PfsGroup</span></span>
<span data-ttu-id="e2c1d-117">Anger PFS-gruppen (Perfect Forward Secrecy).</span><span class="sxs-lookup"><span data-stu-id="e2c1d-117">Specifies the perfect forward secrecy (PFS) group.</span></span>
<span data-ttu-id="e2c1d-118">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="e2c1d-118">Valid values are:</span></span> 

- <span data-ttu-id="e2c1d-119">PFS1</span><span class="sxs-lookup"><span data-stu-id="e2c1d-119">PFS1</span></span> 
- <span data-ttu-id="e2c1d-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="e2c1d-120">None</span></span>

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

### <span data-ttu-id="e2c1d-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="e2c1d-121">-Profile</span></span>
<span data-ttu-id="e2c1d-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e2c1d-122">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e2c1d-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e2c1d-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e2c1d-124">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="e2c1d-124">-SADataSizeKilobytes</span></span>
<span data-ttu-id="e2c1d-125">Anger storleken i kilobyte för säkerhets associationen (SA).</span><span class="sxs-lookup"><span data-stu-id="e2c1d-125">Specifies the size, in kilobytes, of the security association (SA).</span></span>

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

### <span data-ttu-id="e2c1d-126">-SALifetimeSeconds</span><span class="sxs-lookup"><span data-stu-id="e2c1d-126">-SALifetimeSeconds</span></span>
<span data-ttu-id="e2c1d-127">Anger period i sekunder för säkerhets associationen.</span><span class="sxs-lookup"><span data-stu-id="e2c1d-127">Specifies the period, in seconds, of the security association.</span></span>

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

### <span data-ttu-id="e2c1d-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="e2c1d-128">-VNetName</span></span>
<span data-ttu-id="e2c1d-129">Anger det virtuella nätverk som denna cmdlet ställer in IPsec-parametrar för anslutningen till.</span><span class="sxs-lookup"><span data-stu-id="e2c1d-129">Specifies the virtual network for which this cmdlet sets IPsec parameters for the connection.</span></span>

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

### <span data-ttu-id="e2c1d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2c1d-130">CommonParameters</span></span>
<span data-ttu-id="e2c1d-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2c1d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2c1d-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2c1d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2c1d-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2c1d-133">INPUTS</span></span>

## <span data-ttu-id="e2c1d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2c1d-134">OUTPUTS</span></span>

## <span data-ttu-id="e2c1d-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2c1d-135">NOTES</span></span>

## <span data-ttu-id="e2c1d-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2c1d-136">RELATED LINKS</span></span>

[<span data-ttu-id="e2c1d-137">Get-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="e2c1d-137">Get-AzureVNetGatewayIPsecParameters</span></span>](./Get-AzureVNetGatewayIPsecParameters.md)


