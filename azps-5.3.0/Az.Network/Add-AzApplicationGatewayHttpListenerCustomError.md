---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d810afe9f5fcf2a1377f55ffe0822d3e71ee409f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422376"
---
# <span data-ttu-id="dcfad-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="dcfad-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="dcfad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dcfad-102">SYNOPSIS</span></span>
<span data-ttu-id="dcfad-103">Lägger till ett anpassat fel i en http-lyssnare för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="dcfad-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="dcfad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dcfad-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dcfad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dcfad-105">DESCRIPTION</span></span>
<span data-ttu-id="dcfad-106">Cmdleten **Add-AzApplicationGatewayCustomError** lägger till ett anpassat fel i en http-lyssnare för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="dcfad-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="dcfad-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dcfad-107">EXAMPLES</span></span>

### <span data-ttu-id="dcfad-108">Exempel 1: lägger till ett anpassat fel i http Listener Level</span><span class="sxs-lookup"><span data-stu-id="dcfad-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="dcfad-109">Det här kommandot lägger till ett anpassat fel med HTTP-statuskod 502 till http-lyssnaren $listener 01 och returnerar den uppdaterade lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="dcfad-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="dcfad-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dcfad-110">PARAMETERS</span></span>

### <span data-ttu-id="dcfad-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="dcfad-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="dcfad-112">Felsida URL för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="dcfad-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="dcfad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcfad-113">-DefaultProfile</span></span>
<span data-ttu-id="dcfad-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dcfad-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcfad-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="dcfad-115">-HttpListener</span></span>
<span data-ttu-id="dcfad-116">Http-lyssnaren för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="dcfad-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="dcfad-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="dcfad-117">-StatusCode</span></span>
<span data-ttu-id="dcfad-118">Status kod för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="dcfad-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="dcfad-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcfad-119">CommonParameters</span></span>
<span data-ttu-id="dcfad-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcfad-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcfad-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcfad-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcfad-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dcfad-122">INPUTS</span></span>

### <span data-ttu-id="dcfad-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="dcfad-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="dcfad-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dcfad-124">OUTPUTS</span></span>

### <span data-ttu-id="dcfad-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="dcfad-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="dcfad-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dcfad-126">NOTES</span></span>

## <span data-ttu-id="dcfad-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dcfad-127">RELATED LINKS</span></span>

[<span data-ttu-id="dcfad-128">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="dcfad-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="dcfad-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="dcfad-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="dcfad-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="dcfad-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
