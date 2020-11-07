---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 51428d44c2fc5ce29259924f71617317b163ac29
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922047"
---
# <span data-ttu-id="9cf41-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9cf41-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="9cf41-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9cf41-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf41-103">Tar bort URL-sökvägar till en server del.</span><span class="sxs-lookup"><span data-stu-id="9cf41-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="9cf41-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9cf41-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cf41-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9cf41-105">DESCRIPTION</span></span>
<span data-ttu-id="9cf41-106">Cmdleten **Remove-AzApplicationGatewayUrlPathMapConfig** tar bort URL-sökvägar till en server del.</span><span class="sxs-lookup"><span data-stu-id="9cf41-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="9cf41-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9cf41-107">EXAMPLES</span></span>

### <span data-ttu-id="9cf41-108">9.1</span><span class="sxs-lookup"><span data-stu-id="9cf41-108">1:</span></span>
```

```

## <span data-ttu-id="9cf41-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9cf41-109">PARAMETERS</span></span>

### <span data-ttu-id="9cf41-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9cf41-110">-ApplicationGateway</span></span>
<span data-ttu-id="9cf41-111">Anger den Programgateway till vilken denna cmdlet tar bort URL Path Map-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9cf41-111">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="9cf41-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cf41-112">-DefaultProfile</span></span>
<span data-ttu-id="9cf41-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9cf41-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cf41-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="9cf41-114">-Name</span></span>
<span data-ttu-id="9cf41-115">Anger namnet på URL-sökvägen som den här cmdleten tar bort från backend-servern.</span><span class="sxs-lookup"><span data-stu-id="9cf41-115">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="9cf41-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf41-116">CommonParameters</span></span>
<span data-ttu-id="9cf41-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cf41-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf41-118">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cf41-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf41-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9cf41-119">INPUTS</span></span>

### <span data-ttu-id="9cf41-120">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9cf41-120">PSApplicationGateway</span></span>
<span data-ttu-id="9cf41-121">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9cf41-121">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="9cf41-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9cf41-122">OUTPUTS</span></span>

### <span data-ttu-id="9cf41-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9cf41-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9cf41-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9cf41-124">NOTES</span></span>

## <span data-ttu-id="9cf41-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9cf41-125">RELATED LINKS</span></span>

[<span data-ttu-id="9cf41-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9cf41-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9cf41-127">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9cf41-127">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9cf41-128">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9cf41-128">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9cf41-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9cf41-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


