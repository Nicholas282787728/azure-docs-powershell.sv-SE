---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 08447949836af59223572bac1b8fec54f3704d9d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417027"
---
# <span data-ttu-id="58277-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="58277-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="58277-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58277-102">SYNOPSIS</span></span>
<span data-ttu-id="58277-103">Uppdaterar ett anpassat fel i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="58277-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="58277-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58277-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58277-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58277-105">DESCRIPTION</span></span>
<span data-ttu-id="58277-106">Cmdleten **set-AzApplicationGatewayCustomError** uppdaterar ett anpassat fel i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="58277-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="58277-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58277-107">EXAMPLES</span></span>

### <span data-ttu-id="58277-108">Exempel 1: uppdaterar anpassade fel i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="58277-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="58277-109">Det här kommandot uppdaterar det anpassade felet hos HTTP-statuskod 502 i $appgw Gateway, och returnerar den uppdaterade gatewayen.</span><span class="sxs-lookup"><span data-stu-id="58277-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="58277-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58277-110">PARAMETERS</span></span>

### <span data-ttu-id="58277-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="58277-111">-ApplicationGateway</span></span>
<span data-ttu-id="58277-112">Application Gateway</span><span class="sxs-lookup"><span data-stu-id="58277-112">The Application Gateway</span></span>

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

### <span data-ttu-id="58277-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="58277-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="58277-114">Felsida URL för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="58277-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="58277-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58277-115">-DefaultProfile</span></span>
<span data-ttu-id="58277-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="58277-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58277-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="58277-117">-StatusCode</span></span>
<span data-ttu-id="58277-118">Status kod för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="58277-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="58277-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58277-119">CommonParameters</span></span>
<span data-ttu-id="58277-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58277-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58277-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58277-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58277-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58277-122">INPUTS</span></span>

### <span data-ttu-id="58277-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="58277-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="58277-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58277-124">OUTPUTS</span></span>

### <span data-ttu-id="58277-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="58277-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="58277-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58277-126">NOTES</span></span>

## <span data-ttu-id="58277-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58277-127">RELATED LINKS</span></span>

[<span data-ttu-id="58277-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="58277-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="58277-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="58277-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="58277-130">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="58277-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="58277-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="58277-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
