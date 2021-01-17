---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 91de215282dc05be2136237fa5fb2b244d7f0c4a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416072"
---
# <span data-ttu-id="3ecf5-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3ecf5-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="3ecf5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ecf5-102">SYNOPSIS</span></span>
<span data-ttu-id="3ecf5-103">Tar bort ett anpassat fel från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="3ecf5-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="3ecf5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ecf5-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ecf5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ecf5-105">DESCRIPTION</span></span>
<span data-ttu-id="3ecf5-106">Cmdleten **Remove-AzApplicationGatewayCustomError** tar bort ett anpassat fel från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="3ecf5-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="3ecf5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ecf5-107">EXAMPLES</span></span>

### <span data-ttu-id="3ecf5-108">Exempel 1: tar bort det anpassade felet från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="3ecf5-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="3ecf5-109">Detta kommando tar bort det anpassade felet hos HTTP-statuskod 502 från Application Gateway $appgw och returnerar den uppdaterade gatewayen.</span><span class="sxs-lookup"><span data-stu-id="3ecf5-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="3ecf5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ecf5-110">PARAMETERS</span></span>

### <span data-ttu-id="3ecf5-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ecf5-111">-ApplicationGateway</span></span>
<span data-ttu-id="3ecf5-112">Application Gateway</span><span class="sxs-lookup"><span data-stu-id="3ecf5-112">The Application Gateway</span></span>

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

### <span data-ttu-id="3ecf5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ecf5-113">-DefaultProfile</span></span>
<span data-ttu-id="3ecf5-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ecf5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ecf5-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="3ecf5-115">-StatusCode</span></span>
<span data-ttu-id="3ecf5-116">Status kod för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3ecf5-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="3ecf5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ecf5-117">CommonParameters</span></span>
<span data-ttu-id="3ecf5-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ecf5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ecf5-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ecf5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ecf5-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ecf5-120">INPUTS</span></span>

### <span data-ttu-id="3ecf5-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ecf5-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3ecf5-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ecf5-122">OUTPUTS</span></span>

### <span data-ttu-id="3ecf5-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3ecf5-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="3ecf5-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ecf5-124">NOTES</span></span>

## <span data-ttu-id="3ecf5-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ecf5-125">RELATED LINKS</span></span>

[<span data-ttu-id="3ecf5-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3ecf5-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="3ecf5-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3ecf5-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="3ecf5-128">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3ecf5-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="3ecf5-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3ecf5-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
