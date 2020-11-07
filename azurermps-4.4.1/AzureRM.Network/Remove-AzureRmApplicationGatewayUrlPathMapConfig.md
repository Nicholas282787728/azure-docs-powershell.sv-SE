---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 2297eb3d1734938f6c04b22472b02add19f634f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755794"
---
# <span data-ttu-id="a1742-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a1742-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="a1742-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1742-102">SYNOPSIS</span></span>
<span data-ttu-id="a1742-103">Tar bort URL-sökvägar till en server del.</span><span class="sxs-lookup"><span data-stu-id="a1742-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1742-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1742-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1742-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1742-105">DESCRIPTION</span></span>
<span data-ttu-id="a1742-106">Cmdleten **Remove-AzureRmApplicationGatewayUrlPathMapConfig** tar bort URL-sökvägar till en server del.</span><span class="sxs-lookup"><span data-stu-id="a1742-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="a1742-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1742-107">EXAMPLES</span></span>

## <span data-ttu-id="a1742-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1742-108">PARAMETERS</span></span>

### <span data-ttu-id="a1742-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a1742-109">-ApplicationGateway</span></span>
<span data-ttu-id="a1742-110">Anger den Programgateway till vilken denna cmdlet tar bort URL Path Map-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a1742-110">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1742-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="a1742-111">-Name</span></span>
<span data-ttu-id="a1742-112">Anger namnet på URL-sökvägen som den här cmdleten tar bort från backend-servern.</span><span class="sxs-lookup"><span data-stu-id="a1742-112">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1742-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1742-113">-DefaultProfile</span></span>
<span data-ttu-id="a1742-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a1742-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1742-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1742-115">CommonParameters</span></span>
<span data-ttu-id="a1742-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1742-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1742-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1742-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1742-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1742-118">INPUTS</span></span>

### <span data-ttu-id="a1742-119">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a1742-119">PSApplicationGateway</span></span>
<span data-ttu-id="a1742-120">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a1742-120">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="a1742-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1742-121">OUTPUTS</span></span>

### <span data-ttu-id="a1742-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a1742-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a1742-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1742-123">NOTES</span></span>

## <span data-ttu-id="a1742-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1742-124">RELATED LINKS</span></span>

[<span data-ttu-id="a1742-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a1742-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a1742-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a1742-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a1742-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a1742-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a1742-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a1742-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


