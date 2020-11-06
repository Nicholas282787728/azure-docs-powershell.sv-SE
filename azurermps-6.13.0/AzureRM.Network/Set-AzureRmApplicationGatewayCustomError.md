---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: 94a4b4dc41aa1ae7c2a7bb2596018382296f5f87
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576864"
---
# <span data-ttu-id="3a6c4-101">Set-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3a6c4-101">Set-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="3a6c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3a6c4-102">SYNOPSIS</span></span>
<span data-ttu-id="3a6c4-103">Uppdaterar ett anpassat fel i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-103">Updates a custom error in an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a6c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3a6c4-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a6c4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3a6c4-105">DESCRIPTION</span></span>
<span data-ttu-id="3a6c4-106">Cmdleten **set-AzureRmApplicationGatewayCustomError** uppdaterar ett anpassat fel i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-106">The **Set-AzureRmApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="3a6c4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3a6c4-107">EXAMPLES</span></span>

### <span data-ttu-id="3a6c4-108">Exempel 1: uppdaterar anpassade fel i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="3a6c4-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="3a6c4-109">Det här kommandot uppdaterar det anpassade felet hos HTTP-statuskod 502 i $appgw Gateway, och returnerar den uppdaterade gatewayen.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="3a6c4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3a6c4-110">PARAMETERS</span></span>

### <span data-ttu-id="3a6c4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a6c4-111">-ApplicationGateway</span></span>
<span data-ttu-id="3a6c4-112">Application Gateway</span><span class="sxs-lookup"><span data-stu-id="3a6c4-112">The Application Gateway</span></span>

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

### <span data-ttu-id="3a6c4-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="3a6c4-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="3a6c4-114">Felsida URL för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="3a6c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a6c4-115">-DefaultProfile</span></span>
<span data-ttu-id="3a6c4-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a6c4-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="3a6c4-117">-StatusCode</span></span>
<span data-ttu-id="3a6c4-118">Status kod för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="3a6c4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a6c4-119">CommonParameters</span></span>
<span data-ttu-id="3a6c4-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a6c4-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a6c4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a6c4-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3a6c4-122">INPUTS</span></span>

### <span data-ttu-id="3a6c4-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a6c4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3a6c4-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3a6c4-124">OUTPUTS</span></span>

### <span data-ttu-id="3a6c4-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a6c4-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3a6c4-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3a6c4-126">NOTES</span></span>

## <span data-ttu-id="3a6c4-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3a6c4-127">RELATED LINKS</span></span>
