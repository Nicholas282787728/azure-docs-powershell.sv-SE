---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: a33fb510e351a8f1c762801947cf4bbac9a66e28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580288"
---
# <span data-ttu-id="21ed1-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="21ed1-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="21ed1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="21ed1-102">SYNOPSIS</span></span>
<span data-ttu-id="21ed1-103">Ändrar en lokal nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="21ed1-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21ed1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="21ed1-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21ed1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="21ed1-105">DESCRIPTION</span></span>
<span data-ttu-id="21ed1-106">Cmdleten **set-AzureRmLocalNetworkGateway** ändrar en lokal nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="21ed1-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="21ed1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="21ed1-107">EXAMPLES</span></span>

## <span data-ttu-id="21ed1-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="21ed1-108">PARAMETERS</span></span>

### <span data-ttu-id="21ed1-109">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="21ed1-109">-AddressPrefix</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ed1-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21ed1-110">-AsJob</span></span>
<span data-ttu-id="21ed1-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="21ed1-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21ed1-112">-ASN</span><span class="sxs-lookup"><span data-stu-id="21ed1-112">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ed1-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="21ed1-113">-BgpPeeringAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ed1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21ed1-114">-DefaultProfile</span></span>
<span data-ttu-id="21ed1-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="21ed1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21ed1-116">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="21ed1-116">-LocalNetworkGateway</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21ed1-117">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="21ed1-117">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ed1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21ed1-118">CommonParameters</span></span>
<span data-ttu-id="21ed1-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21ed1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21ed1-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21ed1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21ed1-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="21ed1-121">INPUTS</span></span>

### <span data-ttu-id="21ed1-122">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="21ed1-122">PSLocalNetworkGateway</span></span>
<span data-ttu-id="21ed1-123">Parametern ' LocalNetworkGateway ' godkänner värdet av typen ' PSLocalNetworkGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="21ed1-123">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="21ed1-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="21ed1-124">OUTPUTS</span></span>

### <span data-ttu-id="21ed1-125">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="21ed1-125">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="21ed1-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="21ed1-126">NOTES</span></span>

## <span data-ttu-id="21ed1-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="21ed1-127">RELATED LINKS</span></span>

[<span data-ttu-id="21ed1-128">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="21ed1-128">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="21ed1-129">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="21ed1-129">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="21ed1-130">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="21ed1-130">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


