---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 82675befb6a900bacdead036f323959e1e7a72a9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399291"
---
# <span data-ttu-id="b79b6-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b79b6-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="b79b6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b79b6-102">SYNOPSIS</span></span>
<span data-ttu-id="b79b6-103">Tar bort ett anpassat fel från en http-lyssnare för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="b79b6-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="b79b6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b79b6-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b79b6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b79b6-105">DESCRIPTION</span></span>
<span data-ttu-id="b79b6-106">Cmdleten **Remove-AzApplicationGatewayCustomError** tar bort ett anpassat fel från en http-lyssnare för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="b79b6-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="b79b6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b79b6-107">EXAMPLES</span></span>

### <span data-ttu-id="b79b6-108">Exempel 1: tar bort det anpassade felet från en http-lyssnare</span><span class="sxs-lookup"><span data-stu-id="b79b6-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="b79b6-109">Det här kommandot tar bort det anpassade felet hos HTTP-statuskod 502 från http-lyssnaren $listener 01 och returnerar den uppdaterade lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="b79b6-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="b79b6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b79b6-110">PARAMETERS</span></span>

### <span data-ttu-id="b79b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b79b6-111">-DefaultProfile</span></span>
<span data-ttu-id="b79b6-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b79b6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b79b6-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="b79b6-113">-HttpListener</span></span>
<span data-ttu-id="b79b6-114">Http-lyssnaren för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="b79b6-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="b79b6-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="b79b6-115">-StatusCode</span></span>
<span data-ttu-id="b79b6-116">Status kod för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b79b6-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="b79b6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b79b6-117">CommonParameters</span></span>
<span data-ttu-id="b79b6-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b79b6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b79b6-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b79b6-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b79b6-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b79b6-120">INPUTS</span></span>

### <span data-ttu-id="b79b6-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b79b6-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b79b6-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b79b6-122">OUTPUTS</span></span>

### <span data-ttu-id="b79b6-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b79b6-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="b79b6-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b79b6-124">NOTES</span></span>

## <span data-ttu-id="b79b6-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b79b6-125">RELATED LINKS</span></span>

[<span data-ttu-id="b79b6-126">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b79b6-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="b79b6-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b79b6-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="b79b6-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b79b6-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
