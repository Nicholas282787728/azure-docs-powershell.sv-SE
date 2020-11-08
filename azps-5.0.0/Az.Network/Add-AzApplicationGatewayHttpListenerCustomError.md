---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d810afe9f5fcf2a1377f55ffe0822d3e71ee409f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273126"
---
# <span data-ttu-id="62ed2-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="62ed2-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="62ed2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="62ed2-103">Lägger till ett anpassat fel i en http-lyssnare för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="62ed2-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="62ed2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62ed2-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62ed2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62ed2-105">DESCRIPTION</span></span>
<span data-ttu-id="62ed2-106">Cmdleten **Add-AzApplicationGatewayCustomError** lägger till ett anpassat fel i en http-lyssnare för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="62ed2-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="62ed2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62ed2-107">EXAMPLES</span></span>

### <span data-ttu-id="62ed2-108">Exempel 1: lägger till ett anpassat fel i http Listener Level</span><span class="sxs-lookup"><span data-stu-id="62ed2-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="62ed2-109">Det här kommandot lägger till ett anpassat fel med HTTP-statuskod 502 till http-lyssnaren $listener 01 och returnerar den uppdaterade lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="62ed2-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="62ed2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62ed2-110">PARAMETERS</span></span>

### <span data-ttu-id="62ed2-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="62ed2-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="62ed2-112">Felsida URL för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="62ed2-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="62ed2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62ed2-113">-DefaultProfile</span></span>
<span data-ttu-id="62ed2-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="62ed2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62ed2-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="62ed2-115">-HttpListener</span></span>
<span data-ttu-id="62ed2-116">Http-lyssnaren för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="62ed2-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="62ed2-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="62ed2-117">-StatusCode</span></span>
<span data-ttu-id="62ed2-118">Status kod för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="62ed2-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="62ed2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62ed2-119">CommonParameters</span></span>
<span data-ttu-id="62ed2-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62ed2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62ed2-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62ed2-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62ed2-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62ed2-122">INPUTS</span></span>

### <span data-ttu-id="62ed2-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="62ed2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="62ed2-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62ed2-124">OUTPUTS</span></span>

### <span data-ttu-id="62ed2-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="62ed2-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="62ed2-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62ed2-126">NOTES</span></span>

## <span data-ttu-id="62ed2-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62ed2-127">RELATED LINKS</span></span>

[<span data-ttu-id="62ed2-128">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="62ed2-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="62ed2-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="62ed2-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="62ed2-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="62ed2-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
