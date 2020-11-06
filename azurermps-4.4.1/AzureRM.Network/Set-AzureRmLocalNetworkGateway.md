---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 8d2b3c6c15a48407b138fa26778bdf906b5a7a2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575968"
---
# <span data-ttu-id="a8c34-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a8c34-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="a8c34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8c34-102">SYNOPSIS</span></span>
<span data-ttu-id="a8c34-103">Ändrar en lokal nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="a8c34-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8c34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8c34-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8c34-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8c34-105">DESCRIPTION</span></span>
<span data-ttu-id="a8c34-106">Cmdleten **set-AzureRmLocalNetworkGateway** ändrar en lokal nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="a8c34-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="a8c34-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8c34-107">EXAMPLES</span></span>

## <span data-ttu-id="a8c34-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8c34-108">PARAMETERS</span></span>

### <span data-ttu-id="a8c34-109">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a8c34-109">-AddressPrefix</span></span>
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

### <span data-ttu-id="a8c34-110">-ASN</span><span class="sxs-lookup"><span data-stu-id="a8c34-110">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8c34-111">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="a8c34-111">-BgpPeeringAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8c34-112">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a8c34-112">-LocalNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8c34-113">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="a8c34-113">-PeerWeight</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8c34-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8c34-114">-DefaultProfile</span></span>
<span data-ttu-id="a8c34-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8c34-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8c34-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8c34-116">CommonParameters</span></span>
<span data-ttu-id="a8c34-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8c34-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8c34-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8c34-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8c34-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8c34-119">INPUTS</span></span>

### <span data-ttu-id="a8c34-120">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a8c34-120">PSLocalNetworkGateway</span></span>
<span data-ttu-id="a8c34-121">Parametern ' LocalNetworkGateway ' godkänner värdet av typen ' PSLocalNetworkGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a8c34-121">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="a8c34-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8c34-122">OUTPUTS</span></span>

### <span data-ttu-id="a8c34-123">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a8c34-123">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="a8c34-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8c34-124">NOTES</span></span>

## <span data-ttu-id="a8c34-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8c34-125">RELATED LINKS</span></span>

[<span data-ttu-id="a8c34-126">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a8c34-126">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="a8c34-127">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a8c34-127">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="a8c34-128">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a8c34-128">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


