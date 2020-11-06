---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: cc1f6b487d0faf58999a0326a77e01bea74d8c91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574798"
---
# <span data-ttu-id="386c4-101">Remove-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="386c4-101">Remove-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="386c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="386c4-102">SYNOPSIS</span></span>
<span data-ttu-id="386c4-103">Tar bort ett anpassat fel från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="386c4-103">Removes a custom error from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="386c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="386c4-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="386c4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="386c4-105">DESCRIPTION</span></span>
<span data-ttu-id="386c4-106">Cmdleten **Remove-AzureRmApplicationGatewayCustomError** tar bort ett anpassat fel från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="386c4-106">The **Remove-AzureRmApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="386c4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="386c4-107">EXAMPLES</span></span>

### <span data-ttu-id="386c4-108">Exempel 1: tar bort det anpassade felet från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="386c4-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="386c4-109">Detta kommando tar bort det anpassade felet hos HTTP-statuskod 502 från Application Gateway $appgw och returnerar den uppdaterade gatewayen.</span><span class="sxs-lookup"><span data-stu-id="386c4-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="386c4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="386c4-110">PARAMETERS</span></span>

### <span data-ttu-id="386c4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="386c4-111">-ApplicationGateway</span></span>
<span data-ttu-id="386c4-112">Application Gateway</span><span class="sxs-lookup"><span data-stu-id="386c4-112">The Application Gateway</span></span>

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

### <span data-ttu-id="386c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="386c4-113">-DefaultProfile</span></span>
<span data-ttu-id="386c4-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="386c4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="386c4-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="386c4-115">-StatusCode</span></span>
<span data-ttu-id="386c4-116">Status kod för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="386c4-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="386c4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="386c4-117">CommonParameters</span></span>
<span data-ttu-id="386c4-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="386c4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="386c4-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="386c4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="386c4-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="386c4-120">INPUTS</span></span>

### <span data-ttu-id="386c4-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="386c4-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="386c4-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="386c4-122">OUTPUTS</span></span>

### <span data-ttu-id="386c4-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="386c4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="386c4-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="386c4-124">NOTES</span></span>

## <span data-ttu-id="386c4-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="386c4-125">RELATED LINKS</span></span>
