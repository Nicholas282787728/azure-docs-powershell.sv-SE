---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 34f92bfa7566679c4cee9f7a4281ac15c55676b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389436"
---
# <span data-ttu-id="93e9f-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="93e9f-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="93e9f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93e9f-102">SYNOPSIS</span></span>
<span data-ttu-id="93e9f-103">Hämtar anpassade fel från en http-lyssnare av en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="93e9f-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="93e9f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93e9f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93e9f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93e9f-105">DESCRIPTION</span></span>
<span data-ttu-id="93e9f-106">Cmdleten **Get-AzApplicationGatewayCustomError** hämtar anpassade fel från en http-lyssnare av en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="93e9f-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="93e9f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93e9f-107">EXAMPLES</span></span>

### <span data-ttu-id="93e9f-108">Exempel 1: hämtar ett anpassat fel i en http-lyssnare</span><span class="sxs-lookup"><span data-stu-id="93e9f-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="93e9f-109">Det här kommandot hämtar och returnerar det anpassade felet hos HTTP-statuskod 502 från http-lyssnaren $listener 01.</span><span class="sxs-lookup"><span data-stu-id="93e9f-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="93e9f-110">Exempel 2: hämtar listan över alla anpassade fel i en http-lyssnare</span><span class="sxs-lookup"><span data-stu-id="93e9f-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="93e9f-111">Det här kommandot hämtar och returnerar listan över alla anpassade fel från http-lyssnaren $listener 01.</span><span class="sxs-lookup"><span data-stu-id="93e9f-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="93e9f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93e9f-112">PARAMETERS</span></span>

### <span data-ttu-id="93e9f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e9f-113">-DefaultProfile</span></span>
<span data-ttu-id="93e9f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="93e9f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93e9f-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="93e9f-115">-HttpListener</span></span>
<span data-ttu-id="93e9f-116">Http-lyssnaren för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="93e9f-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="93e9f-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="93e9f-117">-StatusCode</span></span>
<span data-ttu-id="93e9f-118">Status kod för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="93e9f-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93e9f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e9f-119">CommonParameters</span></span>
<span data-ttu-id="93e9f-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93e9f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e9f-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93e9f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e9f-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93e9f-122">INPUTS</span></span>

### <span data-ttu-id="93e9f-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="93e9f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="93e9f-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93e9f-124">OUTPUTS</span></span>

### <span data-ttu-id="93e9f-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="93e9f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="93e9f-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93e9f-126">NOTES</span></span>

## <span data-ttu-id="93e9f-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93e9f-127">RELATED LINKS</span></span>

[<span data-ttu-id="93e9f-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="93e9f-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="93e9f-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="93e9f-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="93e9f-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="93e9f-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
