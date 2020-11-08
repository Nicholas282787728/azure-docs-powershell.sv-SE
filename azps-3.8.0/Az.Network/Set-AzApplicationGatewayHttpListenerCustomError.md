---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 3f53bd59e85fa9dac03a99d7e192ce51325ca6a4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089077"
---
# <span data-ttu-id="a1ca3-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a1ca3-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="a1ca3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="a1ca3-103">Uppdaterar ett anpassat fel i en http-lyssnare på en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="a1ca3-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="a1ca3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1ca3-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1ca3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1ca3-105">DESCRIPTION</span></span>
<span data-ttu-id="a1ca3-106">Cmdleten **set-AzApplicationGatewayCustomError** uppdaterar ett anpassat fel i en http-lyssnare för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="a1ca3-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="a1ca3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1ca3-107">EXAMPLES</span></span>

### <span data-ttu-id="a1ca3-108">Exempel 1: uppdaterar ett anpassat fel från en http-lyssnare</span><span class="sxs-lookup"><span data-stu-id="a1ca3-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="a1ca3-109">Det här kommandot uppdaterar det anpassade felet hos HTTP-statuskod 502 i http-lyssnaren $listener 01 och returnerar den uppdaterade lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="a1ca3-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="a1ca3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1ca3-110">PARAMETERS</span></span>

### <span data-ttu-id="a1ca3-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="a1ca3-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="a1ca3-112">Felsida URL för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a1ca3-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="a1ca3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1ca3-113">-DefaultProfile</span></span>
<span data-ttu-id="a1ca3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a1ca3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1ca3-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="a1ca3-115">-HttpListener</span></span>
<span data-ttu-id="a1ca3-116">Http-lyssnaren för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="a1ca3-116">The Application Gateway Http Listener</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1ca3-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="a1ca3-117">-StatusCode</span></span>
<span data-ttu-id="a1ca3-118">Status kod för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a1ca3-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="a1ca3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1ca3-119">CommonParameters</span></span>
<span data-ttu-id="a1ca3-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1ca3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1ca3-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1ca3-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1ca3-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1ca3-122">INPUTS</span></span>

### <span data-ttu-id="a1ca3-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a1ca3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a1ca3-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1ca3-124">OUTPUTS</span></span>

### <span data-ttu-id="a1ca3-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a1ca3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="a1ca3-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1ca3-126">NOTES</span></span>

## <span data-ttu-id="a1ca3-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1ca3-127">RELATED LINKS</span></span>

[<span data-ttu-id="a1ca3-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a1ca3-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="a1ca3-129">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a1ca3-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="a1ca3-130">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a1ca3-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)