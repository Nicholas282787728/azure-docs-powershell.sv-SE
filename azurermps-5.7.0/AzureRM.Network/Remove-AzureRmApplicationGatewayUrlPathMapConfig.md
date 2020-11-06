---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 612e6b0cb5438dbb37a2e9d1c77da151c852fac1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576489"
---
# <span data-ttu-id="dc3ce-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="dc3ce-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="dc3ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc3ce-102">SYNOPSIS</span></span>
<span data-ttu-id="dc3ce-103">Tar bort URL-sökvägar till en server del.</span><span class="sxs-lookup"><span data-stu-id="dc3ce-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc3ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc3ce-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc3ce-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc3ce-105">DESCRIPTION</span></span>
<span data-ttu-id="dc3ce-106">Cmdleten **Remove-AzureRmApplicationGatewayUrlPathMapConfig** tar bort URL-sökvägar till en server del.</span><span class="sxs-lookup"><span data-stu-id="dc3ce-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="dc3ce-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc3ce-107">EXAMPLES</span></span>

## <span data-ttu-id="dc3ce-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc3ce-108">PARAMETERS</span></span>

### <span data-ttu-id="dc3ce-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc3ce-109">-ApplicationGateway</span></span>
<span data-ttu-id="dc3ce-110">Anger den Programgateway till vilken denna cmdlet tar bort URL Path Map-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dc3ce-110">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc3ce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc3ce-111">-DefaultProfile</span></span>
<span data-ttu-id="dc3ce-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dc3ce-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc3ce-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="dc3ce-113">-Name</span></span>
<span data-ttu-id="dc3ce-114">Anger namnet på URL-sökvägen som den här cmdleten tar bort från backend-servern.</span><span class="sxs-lookup"><span data-stu-id="dc3ce-114">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="dc3ce-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc3ce-115">CommonParameters</span></span>
<span data-ttu-id="dc3ce-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc3ce-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc3ce-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc3ce-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc3ce-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc3ce-118">INPUTS</span></span>

### <span data-ttu-id="dc3ce-119">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc3ce-119">PSApplicationGateway</span></span>
<span data-ttu-id="dc3ce-120">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="dc3ce-120">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="dc3ce-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc3ce-121">OUTPUTS</span></span>

### <span data-ttu-id="dc3ce-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc3ce-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dc3ce-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc3ce-123">NOTES</span></span>

## <span data-ttu-id="dc3ce-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc3ce-124">RELATED LINKS</span></span>

[<span data-ttu-id="dc3ce-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="dc3ce-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="dc3ce-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="dc3ce-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="dc3ce-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="dc3ce-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="dc3ce-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="dc3ce-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


